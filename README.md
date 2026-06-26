# Telemetry Store

## Overview
The **Telemetry Store** service is responsible for aggregating, storing, and serving telemetry metrics related to application and cluster health. It processes health checks, performance data, and other critical metrics needed by the monitoring dashboard.

## Features
- Stores application logs, metrics, and health telemetry.
- Exposes querying capabilities for frontend dashboards.
- Integrates with external blob storage or persistent databases as needed.
- Built with Python and FastAPI.

## Getting Started

### Prerequisites
- Python 3.10+
- `pip` package manager
- Docker (optional for containerized deployment)

### Installation
1. Navigate to the service directory:
   ```bash
   cd services/telemetry-store
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Service
To run the service locally for development:
```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

## Docker
Build the Docker image:
```bash
docker build -t incident-tracker/telemetry-store .
```
Run the Docker container:
```bash
docker run -p 8000:8000 incident-tracker/telemetry-store
```
