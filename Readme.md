# SAP Production Automation & Material Reservation

> **Copyright & Usage Notice**  
> Copyright © 2026 Aditya Sarkale. All rights reserved **to the extent of rights owned by the author**.  
> No license is granted to copy, modify, redistribute, publish, sublicense, or use this source code or substantial portions of it outside the GitHub platform without prior written permission from the applicable rights holder.  
> **Important:** Any company-owned, client-owned, SAP-proprietary, third-party, or otherwise restricted material remains subject to its applicable ownership, confidentiality, and licensing terms.

## Overview
Python-based SAP GUI automation for production and material-reservation workflows, including processes involving **CO11N, MB21 and VL01N**.

## Capabilities
- Production-order confirmation automation
- Material reservation workflows
- Excel/CSV-driven processing
- SAP GUI navigation
- Error handling and result logging
- Single and multi-operation processing

## Architecture
```
Input Excel/CSV
      ↓
Python / Flask
      ↓
SAP GUI Scripting (pywin32)
      ↓
SAP transactions
      ↓
Result / status logging
```

## Repository Structure
- `backend/` — Python/SAP automation
- `frontend/` — React UI
- `Readme.md` — project documentation

## Prerequisites
- Windows
- SAP GUI for Windows
- SAP GUI Scripting enabled
- Python 3.10+
- Node.js/npm for frontend
- Appropriate SAP authorization

## Setup

### Backend
Use the Python entry point and dependency files present in the relevant backend directory. Where a `requirements.txt` exists:
```powershell
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

Start the backend using the entry point documented by the current project files.

### Frontend
```powershell
cd frontend
npm install
npm start
```

## SAP GUI Scripting / RZ11
If SAP is logged in but automation reports **"SAP not logged in or User cancelled the transaction"**, verify:
- SAP GUI is running.
- The correct session is active.
- The required RZ11 dynamic scripting parameter is **TRUE**.
- The transaction has not been manually cancelled.

Server-side changes must be handled by the authorized SAP Basis team.

## Security
Do not commit credentials, tokens, confidential company data or production files. Use approved secret-management mechanisms.

## License / Rights
This repository previously contained an open-source license notice. That notice has been removed in favor of the proprietary rights notice above. No open-source license is granted by this repository.

## Author
**Aditya Sarkale** — https://github.com/AdiSarkale
