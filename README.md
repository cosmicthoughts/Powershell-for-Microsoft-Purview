# Powershell-for-Microsoft-Purview

This guide outlines the essential setup steps for working with Microsoft Purview via PowerShell, including module installation and connection commands.

---

## Install Required PowerShell Module

To manage Microsoft Purview (and Exchange Online) from PowerShell, install the `ExchangeOnlineManagement` module:

```powershell
Install-Module -Name ExchangeOnlineManagement -Scope CurrentUser -Force
Import-Module ExchangeOnlineManagement
```

## Connect to Microsoft Purview and Exchange Online

You’ll typically need both sessions connected to work with Microsoft Purview effectively

```powershell
Connect-ExchangeOnline
Connect-IPPSSession
```

---

## Check if Unified Audit Logging is Enabled
Confirms whether unified audit log collection is active across Microsoft 365.
```powershell
Get-AdminAuditLogConfig | Select UnifiedAuditLogIngestionEnabled
```

## Search Unified Audit Log for User Activity
