# MSE-2 Software Engineering and DevOps Practical Examination
## Full-Stack Application Containerization & CI/CD Deployment

---

## 1. Student Information

| Field | Details |
|---|---|
| **Full Name** | Abhishek Kumar |
| **University Roll Number** | 202401100300007 |
| **Section** | A |
| **Branch** | CSE-AI |
| **College** | KIET Deemed to be University |
| **GitHub Username** | abhiishek892 |
| **Docker Hub Username** | abhiishek89 |

---

## 2. GitHub Submission Details

- **Personal Fork Repository URL:** [https://github.com/abhiishek892/MSE-2-SSED-Morning](https://github.com/abhiishek892/MSE-2-SSED-Morning)
- **Implementation Branch:** `main`
- **Original Starter Repository:** [https://github.com/atindeRR/MSE-2-SSED-Morning](https://github.com/atindeRR/MSE-2-SSED-Morning)

> **Important Discrepancy Note:** The examination README mentions the instructor's base repository as `taskflow-docker`, whereas the provided upstream starter repository is `MSE-2-SSED-Morning`. Please select the appropriate base repository as instructed by your invigilator during PR creation.

---

## 3. Docker Hub Image Repositories

| Component | Published Image Reference | Docker Hub URL |
|---|---|---|
| **Frontend** | `abhiishek89/mse-2-ssed-morning-frontend:latest`<br>`abhiishek89/taskflow-frontend:latest` | `https://hub.docker.com/r/abhiishek89/mse-2-ssed-morning-frontend` |
| **Backend** | `abhiishek89/mse-2-ssed-morning-backend:latest`<br>`abhiishek89/taskflow-backend:latest` | `https://hub.docker.com/r/abhiishek89/mse-2-ssed-morning-backend` |

---

## 4. Local Verification & Testing Results

All 12 automated API tests executed and passed against the containerized stack:

```text
PASS ./api.test.js
  TaskFlow deployed API
    √ TC01: health endpoint confirms API, PostgreSQL and Redis (34 ms)
    √ TC02: register a user (123 ms)
    √ TC03: reject duplicate email (86 ms)
    √ TC04: login and receive token (105 ms)
    √ TC05: reject unauthenticated task request (6 ms)
    √ TC06: create a task (18 ms)
    √ TC07: list tasks and populate cache (12 ms)
    √ TC08: subsequent list can be served from Redis (7 ms)
    √ TC09: update task status and invalidate cache (12 ms)
    √ TC10: reject invalid task status (7 ms)
    √ TC11: delete task (8 ms)
    √ TC12: deleted task is no longer in list (7 ms)

Test Suites: 1 passed, 1 total
Tests:       12 passed, 12 total
```

- **PostgreSQL Persistence:** Verified using named volume `taskflow_postgres_data`. Test data persisted across `docker restart taskflow-postgres`.
- **Redis Caching:** Verified cache hit (`redis-cache`) on repeated task retrieval and cache invalidation on task mutation.
- **Hadolint Linting:** 0 violations on both `frontend/Dockerfile` and `backend/Dockerfile`.

---

## 5. CI/CD Execution Evidence (Screenshots)

*Instructions: Capture screenshots from your GitHub Actions run and paste them below before converting to PDF (`ROLL_NUMBER_STUDENT_NAME.pdf`).*

### 5.1 GitHub Actions Workflow Execution
*(Attach screenshot showing the workflow triggered on the `main` branch under GitHub Actions)*

```text
[ INSERT SCREENSHOT: GitHub Actions Workflow Overview ]
```

---

### 5.2 Docker Hub Authentication Step
*(Attach screenshot showing successful login to Docker Hub via `docker/login-action`)*

```text
[ INSERT SCREENSHOT: Login to Docker Hub stage in CD pipeline ]
```

---

### 5.3 Backend Docker Image Build and Publishing
*(Attach screenshot of backend image build and push to Docker Hub)*

```text
[ INSERT SCREENSHOT: Build and push backend stage ]
```

---

### 5.4 Frontend Docker Image Build and Publishing
*(Attach screenshot of frontend multi-stage build and push to Docker Hub)*

```text
[ INSERT SCREENSHOT: Build and push frontend stage ]
```

---

### 5.5 Docker Compose Image Pull
*(Attach screenshot of `docker compose -f docker-compose.deploy.yml pull` execution)*

```text
[ INSERT SCREENSHOT: Pull published images stage ]
```

---

### 5.6 Application Deployment
*(Attach screenshot of `docker compose -f docker-compose.deploy.yml up -d` execution)*

```text
[ INSERT SCREENSHOT: Deploy using Docker Hub images stage ]
```

---

### 5.7 Backend Health Verification
*(Attach screenshot of `http://localhost:3000/health` returning status 200 with `postgres: ok` and `redis: ok`)*

```text
[ INSERT SCREENSHOT: Backend health verification curl log ]
```

---

### 5.8 Frontend Accessibility Verification
*(Attach screenshot of `http://localhost:8080/` HTTP 200 response and browser view)*

```text
[ INSERT SCREENSHOT: Frontend accessibility curl / browser test ]
```

---

### 5.9 Final Successful CI/CD Pipeline
*(Attach screenshot showing all green checkmarks for the completed workflow)*

```text
[ INSERT SCREENSHOT: Overall successful GitHub Actions workflow run ]
```

---

### 5.10 Instructor CI Evaluation Results (if applicable)
*(Attach screenshot of the PR CI Evaluation run `ci.yml` if available)*

```text
[ INSERT SCREENSHOT: Instructor CI Evaluation Workflow Results ]
```

---

## 6. Student Declaration

"I hereby declare that the submitted Docker implementation is my own work. I have successfully executed and verified the required CI/CD pipeline stages, published the Docker images to my Docker Hub account, and tested the application deployment."

- **Student Name:** Abhishek Kumar
- **Date:** 18/11/2026
- **College:** KIET Deemed to be University
