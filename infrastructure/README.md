# Infrastructure Management

This directory contains instructions for managing the local search and crawling environment for the Forensic Transcript Analyst.

## Services Included
1. **SearxNG**: Privacy-focused meta-search engine exposing a clean interface and JSON API.
   - Address: `http://localhost:8080`
2. **Crawl4AI**: High-performance crawling service for LLM-ready markdown extraction.
   - Address: `http://localhost:11235`

---

## Instructions

### 1. Start the Environment
To build, recreate, and start all containers in the background:
```bash
docker compose up -d
```

### 2. Stop the Environment
To stop the running containers without deleting volumes (keeps search settings and crawl cache):
```bash
docker compose stop
```

To stop and remove the containers, networks, and volumes:
```bash
docker compose down -v
```

### 3. Check Status & Logs
To verify which containers are active:
```bash
docker compose ps
```

To view the live log streams for all services:
```bash
docker compose logs -f
```

### 4. Update the Services
To pull the latest images and restart the services:
```bash
docker compose pull
docker compose up -d
```

---

## Important Considerations
- **Port Conflicts**: Ensure that ports `8080` and `11235` are free on your host machine before starting.
- **Persistent Data**: 
  - SearxNG configuration is located in `./searxng/settings.yml`.
  - Crawl4AI cache and browser profiles are stored in `./crawl4ai/`.
