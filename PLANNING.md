# Access Control Data Migration Framework

## Purpose
A web app to convert data between four access control systems (Avigilon Unity Access, Verkada Access, Avigilon Alta Access, Acre Access), supporting bidirectional CSV and API integrations, multiple input formats (CSV, RTF, Excel, PDF, SQL backups), AI-driven mapping with UI-prompted API keys, and robust security.

## Architecture
- Client-server with modular services.
- Frontend: React, Tailwind CSS.
- Backend API: Go (Gin, GORM).
- File Processor: Python (pandas, PyPDF2, pyodbc).
- AI Service: Python (langchain, FastAPI).
- Database: PostgreSQL.
- Storage: Local filesystem (AES-256).
- Auth: Keycloak (OAuth 2.0, zero-trust).
- Orchestration: Proxmox LXC/VMs via Proxmox MCP.
- Security: Nginx (TLS 1.3), Python cryptography.

## Constraints
- Local macOS development, Proxmox test deployments.
- Verified libraries (pandas==2.2.*, PyPDF2==3.0.*, langchain==0.3.*, Gin==1.9.*, GORM==1.25.*).
- No LLM hallucinations, full documentation.
- 60% manual, 40% automated testing.