# Security Updates

This document tracks security updates and CVE fixes for oauth2-proxy.

## Recently Fixed CVEs

### 2025-01-29

- **CVE-2025-40909** (perl-base, HIGH): Fixed by updating Alpine base image from 3.22.1 to 3.23.7
- **CVE-2019-1010022** (libc6, HIGH): Fixed by updating distroless base image to use debian12 variant

## Security Scanning

We use automated security scanning to detect vulnerabilities:

1. **Trivy** - Container image vulnerability scanning
2. **govulncheck** - Go-specific vulnerability scanning  
3. **Nancy** - OSS Index dependency scanning
4. **CodeQL** - Static analysis security testing

## Security Update Process

1. Automated dependency updates via Renovate
2. Daily security scans via GitHub Actions
3. Manual security reviews for critical vulnerabilities
4. Immediate patching for HIGH/CRITICAL severity issues

## Reporting Security Issues

Please report security vulnerabilities privately via GitHub Security Advisories or email the maintainers directly.

## Base Image Updates

We regularly update our base images to ensure the latest security patches:

- **Build Image**: `golang:1.24.5-bookworm` - Updated regularly for Go security patches
- **Runtime Image (Distroless)**: `gcr.io/distroless/static:nonroot-debian12` - Updated for Debian security patches  
- **Runtime Image (Alpine)**: `alpine:3.23.7` - Updated for Alpine security patches

## Monitoring

- Security scans run daily at 2 AM UTC
- Critical/High severity vulnerabilities trigger immediate alerts
- Dependency updates are grouped and scheduled weekly
