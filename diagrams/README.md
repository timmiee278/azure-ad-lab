## Architecture Diagram

                🌐 Azure Cloud
                      |
                      v
        ┌──────────────────────────────┐
        │ Windows Server (Domain Ctrl) │
        │ Active Directory (AD DS)     │
        │ Domain: itlab.local          │
        └──────────────┬───────────────┘
                       |
        ┌──────────────┼──────────────┐
        |                              |
        v                              v
┌──────────────────┐      ┌─────────────────────┐
│ Organizational   │      │ Group Policy (GPO)  │
│ Units (OU)       │      │ IT-Policy           │
│ Users (jcastro)  │      │ RDP restrictions    │
└─────────┬────────┘      └─────────┬───────────┘
          |                          |
          v                          v
     ┌────────────────────────────────────┐
     │ Remote Desktop Services (RDP)      │
     │ Controlled Access to VM            │
     └────────────────────────────────────┘
                      |
                      v
               🖥️ User Access
