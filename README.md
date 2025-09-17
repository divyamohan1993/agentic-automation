# 🚀 Agentic Automation

## Overview

This repository contains a minimal Flask web application designed specifically for **Jenkins CI/CD automation testing**. The application serves as a simple test target for continuous integration and deployment pipelines.

## Purpose

- **Jenkins CI/CD Testing**: Primary purpose is to provide a straightforward application for testing Jenkins automation workflows
- **Deployment Verification**: Enables validation of automated deployment processes
- **Pipeline Testing**: Serves as a reliable target for CI/CD pipeline development and testing

## Application Structure

```
agentic-automation/
├── app.py                 # Main Flask application
├── templates/
│   └── index.html        # Landing page template
├── .gitignore           # Python gitignore rules
└── README.md            # This file
```

## Technical Details

- **Framework**: Flask (Python)
- **Port**: 8080
- **Environment**: Designed for containerized deployments
- **Dependencies**: Minimal - only Flask required

## Quick Start

### Prerequisites
- Python 3.x
- Flask (`pip install flask`)

### Running Locally

```bash
# Clone the repository
git clone https://github.com/divyamohan1993/agentic-automation.git
cd agentic-automation

# Install dependencies
pip install flask

# Run the application
python app.py
```

The application will be available at `http://localhost:8080`

### Docker Deployment

For containerized deployment in Jenkins pipelines:

```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY . .
RUN pip install flask
EXPOSE 8080
CMD ["python", "app.py"]
```

## Jenkins Integration

This application is specifically designed to work with Jenkins automation workflows:

1. **Source Code Management**: Git integration for automated pulls
2. **Build Process**: Simple Python application build
3. **Testing**: Basic application startup and health checks
4. **Deployment**: Container-based deployment verification
5. **Monitoring**: Simple HTTP endpoint for status monitoring

## Features

- ✅ Minimal dependencies for reliable builds
- ✅ Simple HTTP endpoint for health checks
- ✅ Containerization-ready
- ✅ Comprehensive logging for debugging
- ✅ Production-ready error handling

## API Endpoints

- `GET /` - Main landing page with application status

## Contributing

This repository is maintained for Jenkins CI/CD automation testing purposes. Contributions should focus on improving the application's reliability as a test target.

## License

MIT License - See [LICENSE](LICENSE) file for details

---

**Note**: This application is specifically designed for Jenkins CI/CD automation testing and may be updated to support additional automation frameworks in the future.
