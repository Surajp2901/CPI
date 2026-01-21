# SAP CPI – Order Hub Integration

This repository contains SAP Integration Suite (CPI) artifacts developed for an 
Order Hub scenario, enabling automated Sales Order creation in SAP S/4HANA 
from external systems.

---

## Business Problem
- Manual order entry between third-party applications and SAP S/4HANA
- Delays, data inconsistencies, and manual errors
- No real-time visibility across systems

---

## Solution Overview
- Automated Order Hub iFlow built using SAP CPI
- Orders received via HTTPS in JSON format
- Transformed and posted to SAP S/4HANA using OData services
- Order creation response sent back to source system

---

## Integration Flow (High Level)
1. HTTPS Sender receives JSON order from external system
2. Payload converted and enriched with SAP master data
3. Message mapping converts payload to SAP Sales Order format
4. OData Adapter creates Sales Order in SAP S/4HANA
5. Sales Order ID returned to calling system
6. Event published for downstream consumers
7. Errors handled via dedicated exception subprocess

---

## Key Capabilities
- Real-time Sales Order creation
- Data enrichment and validation
- Secure API exposure via SAP API Management
- Event-driven integration using Advanced Event Mesh
- Robust error handling and monitoring

---

## Security
- OAuth 2.0 authentication using XSUAA
- JWT token validation via API Management
- Secure credential handling using Key Value Maps (KVM)

---

## Event-Driven Integration
- Sales Order creation events published to Solace Queue
- Supports asynchronous and loosely coupled integrations
- Reliable delivery for downstream systems

---

## Transport & Governance
- Integration content transported using SAP CTMS
- DEV → PROD landscape promotion
- Centralized and controlled deployment process

---

## Repository Structure
- CPI artifacts uploaded as exported ZIP files
- Organized by integration packages

> Note: CPI iFlows are provided as ZIP exports since CPI artifacts 
> cannot be represented as readable source code in Git repositories.
