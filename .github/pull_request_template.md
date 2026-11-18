## Student Details

- **Name:** Abhishek Kumar
- **Roll Number:** 202401100300007
- **Section:** A
- **Branch:** CSE-AI
- **College:** KIET Deemed to be University
- **GitHub Username:** abhiishek892
- **Docker Hub Username:** abhiishek89

## Docker Hub Images

- **Frontend Image:** `abhiishek89/mse-2-ssed-morning-frontend:latest` (also tagged `abhiishek89/taskflow-frontend:latest`)
- **Backend Image:** `abhiishek89/mse-2-ssed-morning-backend:latest` (also tagged `abhiishek89/taskflow-backend:latest`)

## Application Deployment

- **Application URL:** `http://localhost:8080/`
- **Backend Health URL:** `http://localhost:3000/health`
- **Deployment Status:** PASSED

## Implementation Checklist

- [x] Frontend Dockerfile implemented (Multi-stage Vite build + Nginx alpine reverse proxy)
- [x] Backend Dockerfile implemented (Node 20 alpine, non-root user 1000:1000, npm start)
- [x] docker-compose.yml implemented (Orchestrates frontend, backend, postgres, redis with health checks)
- [x] docker-compose.deploy.yml implemented (Image-based deployment using published Docker Hub images)
- [x] Frontend image published to Docker Hub
- [x] Backend image published to Docker Hub
- [x] PostgreSQL persistence verified (Named volume `taskflow_postgres_data` verified across restarts)
- [x] Redis caching verified (In-memory task caching and cache invalidation tested)
- [x] Application functionality tested (12/12 automated Supertest Jest tests passed)
- [x] CD pipeline passed successfully
- [x] Latest changes committed and pushed

## CI/CD Verification

- **CD Workflow Run URL:** https://github.com/abhiishek892/MSE-2-SSED-Morning/actions/runs/44250120568
- **Final Workflow Status:** PASSED

## Declaration

I confirm that the implementation submitted is my own work and that I have tested the containerized application.

