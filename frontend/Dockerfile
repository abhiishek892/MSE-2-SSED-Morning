# Multi-stage Dockerfile for TaskFlow Frontend
# Stage 1: Build the React application with Vite
FROM node:20-alpine AS build

WORKDIR /app

# Copy package manifests first to leverage Docker layer caching
COPY package*.json ./

# Install dependencies required for Vite build
RUN npm install

# Copy application source code
COPY . .

# Build production assets to /app/dist
RUN npm run build

# Stage 2: Serve the production build using lightweight Nginx
FROM nginx:alpine

# Copy custom Nginx configuration with reverse proxy rules
COPY nginx.conf /etc/nginx/conf.d/default.conf

# Copy compiled static assets from the build stage
COPY --from=build /app/dist /usr/share/nginx/html

# Expose container HTTP port
EXPOSE 80

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
