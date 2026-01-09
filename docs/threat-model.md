# Threat Model

This document defines the security assumptions and threat boundaries
for the MIKA Private Cloud.

## Security Model
- No public IP exposure
- No port forwarding
- All access through WireGuard
- No third-party cloud services
- Admin-controlled credentials

## Assets
- User data
- AI training datasets
- VPN keys
- Configuration files

## Trust Assumptions
- Physical access is trusted
- VPN peers are authorized
- Admin device is uncompromised

## Threat Actors
- Unauthorized LAN users
- Compromised clients
- Configuration mistakes

## Mitigations
- WireGuard-only access
- Least-privilege services
- Filesystem permission isolation
