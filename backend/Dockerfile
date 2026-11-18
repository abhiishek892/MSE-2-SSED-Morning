# Backend Dockerfile for TaskFlow API
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Set default production environment
ENV NODE_ENV=production \
    PORT=3000

# Copy package manifests first for caching
COPY package*.json ./

# Install production dependencies
RUN npm install --omit=dev

# Copy application source code with proper ownership for non-root user
COPY --chown=node:node . .

# Switch to the non-root 'node' user (UID:GID 1000:1000)
USER 1000:1000

# Expose backend service port
EXPOSE 3000

# Application startup command matching package.json
CMD ["npm", "start"]
