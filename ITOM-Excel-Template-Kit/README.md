# OribiServ ITOM Public Website

Public front-end for the ITOM/ITSM template kit.

## Access

The site may be hosted publicly. The operational workspace is intended to require GitHub OAuth and to permit only the GitHub account **NazeerK**.

GitHub Pages alone cannot securely enforce identity. Use a server-side OAuth callback/serverless function, verify the GitHub account, establish a secure session, and enforce the allowlist before exposing operational data.

Never put OAuth client secrets, GitHub access tokens, passwords, or a trusted username check in browser JavaScript.

## Modules

Command Center, Service Desk, Incidents, Problems, Changes, Releases, SLA/OLA, Monitoring, Assets/CMDB, Network, Servers, Applications, Software, Backup/DR, Vendors, Risk/Controls, Finance, Capacity, Automation, Knowledge, Runbooks, SOP, Continual Improvement, Planning, On-Call, Handover and RACI.

## Hosting

This folder can be published through GitHub Pages as the public site. For real authentication and live data, pair it with a backend/API on a platform that supports OAuth/session handling, or place the protected application behind an authenticated gateway.
