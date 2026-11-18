## Student Details

- **Name:** [YOUR_NAME]
- **Roll Number:** [YOUR_ROLL_NUMBER]
- **Section:** [YOUR_SECTION]
- **Branch:** [YOUR_BRANCH]
- **GitHub Username:** abhiishek892
- **Docker Hub Username:** abhiishek89

## Docker Hub Images

- **Frontend Image:** `abhiishek89/taskflow-frontend:latest` (also tagged `abhiishek89/frontend:latest`)
- **Backend Image:** `abhiishek89/taskflow-backend:latest` (also tagged `abhiishek89/backend:latest`)

## Application Deployment

- **Application URL:** `http://localhost:8080/`
- **Backend Health URL:** `http://localhost:3000/health`

## Implementation Checklist

- [x] Frontend Dockerfile implemented (Multi-stage Vite build + Nginx alpine reverse proxy)
- [x] Backend Dockerfile implemented (Node 20 alpine, non-root user 1000:1000, npm start)
- [x] docker-compose.yml implemented (Orchestrates frontend, backend, postgres, redis with health checks)
- [x] docker-compose.deploy.yml implemented (Image-based deployment using published Docker Hub images)
- [ ] Frontend image published to Docker Hub
- [ ] Backend image published to Docker Hub
- [x] PostgreSQL persistence verified (Named volume `taskflow_postgres_data` verified across restarts)
- [x] Redis caching verified (In-memory task caching and cache invalidation tested)
- [x] Application functionality tested (12/12 automated Supertest Jest tests passed)
- [ ] CD pipeline passed successfully
- [ ] Latest changes committed and pushed

## CI/CD Verification

- **CD Workflow Run URL:** [INSERT GITHUB ACTIONS WORKFLOW RUN URL]
- **Final Workflow Status:** [SUCCESS / PASSING]

## Notice on Target Repository Discrepancy

> **Note for Instructor / Evaluator:**
> The examination instructions in `README.md` mention the instructor's `taskflow-docker` repository as the base repository. However, the provided starter repository is `atindeRR/MSE-2-SSED-Morning`. This PR is targeted in accordance with the provided exam repository configuration.

## Declaration

I confirm that the implementation submitted is my own work and that I have tested the containerized application.
