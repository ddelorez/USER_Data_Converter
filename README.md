# Access Control Data Migration Framework

A web app to convert data between four access control systems (Avigilon Unity Access, Verkada Access, Avigilon Alta Access, Acre Access) using CSV and API integrations, with AI-driven field mapping and robust security.

## Features
- Bidirectional data conversion between four access control systems via CSV and API.
- Support for multiple input formats (CSV, RTF, Excel, PDF, SQL backups).
- AI-driven field mapping with user-provided API keys, prompted via UI.
- Secure data handling with TLS 1.3, AES-256 encryption, and zero-trust architecture.
- Manual and automated testing for reliability and accuracy.

## Setup
1. Clone the repo: `git clone <repo-url>`.
2. Install frontend dependencies: `npm install` (in `/src/frontend`).
3. Install backend dependencies: `go mod tidy` (in `/src/backend`).
4. Install Python dependencies: `pip install -r requirements.txt` (in `/src/processor`).
5. Configure Proxmox LXC containers via Proxmox MCP in Kilo Code.
6. Set up PostgreSQL database locally or in a Proxmox container.
7. Run locally on macOS:
   - Frontend: `npm start` (in `/src/frontend`).
   - Backend API: `go run .` (in `/src/backend`).
   - AI Service: `fastapi run` (in `/src/processor`).
8. Access the app at `http://localhost:3000`.

## Project Structure
- `/src`: Source code (React, Go, Python).
- `/samples`: Sample import/export documents.
- `/docs`: System-specific rules and setup guides.
- `/data`: Input file storage.
- `/output`: Generated CSV/API payloads.
- `/config`: Encrypted config files (API keys).
- `/tests`: Automated test scripts.
- `PLANNING.md`: Project vision and architecture.
- `TASK.md`: Task tracking.
- `README.md`: This file.

## Development
- Use Kilo Code’s Architect mode with Proxmox MCP for container management.
- Follow LLM rules: verified libraries, prompt for API details, no hallucinations, full documentation.
- Run 60% manual and 40% automated tests (in `/tests`).

## Future Plans
- Expand to additional systems (e.g., Genetec, Lenel).
- Migrate to Linode for cloud hosting.