# Mivibzzz WebMonitor
**Online Monitoring & Alerts Platform**

**Live Service:** https://webmonitor.mivibzzz.com/

---

## Project Overview

**Mivibzzz WebMonitor** is the official website monitoring and alerting platform for **Mivibzzz.com**.  
Formerly known as **MerySpeak**, the service has been fully integrated into the Mivibzzz ecosystem and now operates as its dedicated uptime, performance, and security monitoring solution.

WebMonitor provides real-time visibility into website availability, response times, SSL certificates, security headers, page integrity, and domain expiration—helping site owners detect issues early and maintain reliable, secure online services.

---

## Relationship to MerySpeak

- **MerySpeak** is now a legacy product and service name under the **Mivibzzz** brand
- This repository is the **canonical source** for Mivibzzz’s monitoring platform
- `webmonitor.mivibzzz.com` is the primary production endpoint
- The MerySpeak.com repository will be updated to reference this project

---

## Technology Stack

| Category | Technology |
|--------|-----------|
| Framework | Flask 3.0.0 |
| Database | SQLite with SQLAlchemy 2.0.23 |
| Background Jobs | APScheduler 3.10.4 (ThreadPoolExecutor) |
| Payments | Stripe 7.8.0 |
| HTTP Clients | Requests 2.31.0, HTTPX 0.26.0 |
| SSL / Crypto | Cryptography 41.0.7, PyOpenSSL 23.3.0 |
| DNS / Domain | dnspython 2.4.2, python-whois 0.8.0 |
| Email | Gmail SMTP |
| Frontend | Vanilla JavaScript, Chart.js |

---

## Core Features

### Uptime Monitoring
Continuous HTTP monitoring with instant alerts when services go down or recover.

### Response Time Analytics
Tracks **Time To First Byte (TTFB)** with trend analysis, percentiles, and performance alerts.

### SSL Certificate Monitoring
Expiration tracking, issuer details, and early renewal notifications.

### Page Change Detection
SHA256 content hashing to detect defacements, injected scripts, or unauthorized edits.

### Domain Expiry & DNS Monitoring
WHOIS expiration tracking and monitoring of A, AAAA, CNAME, MX, TXT, and NS records.

### Security Headers Analysis
Automated scoring and actionable recommendations for HTTP security headers.

### Status Page Widget
Embeddable real-time uptime widget for public transparency.

### Alerts & Notifications
Downtime, recovery, SSL expiry, and weekly performance summary emails.

---

## Status Widget Embed

```html
<script src="https://webmonitor.mivibzzz.com/static/js/embed.js"
        data-website-id="YOUR_WEBSITE_ID"
        data-theme="light"></script>

## Widget API
### Endpoint

GET /api/widget/{website_id}

### Example Response
{
  "success": true,
  "data": {
    "status": "up",
    "uptime_24h": 100.0,
    "uptime_7d": 99.95,
    "uptime_30d": 99.87,
    "last_checked": "2025-01-15T10:30:00Z",
    "last_incident": "2025-01-10T08:15:00Z"
  }
}

CORS is enabled to allow cross-domain access.
