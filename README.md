# Mivibzzz.com  
## Online Monitoring and Alerts

## Live At https://webmonitor.mivibzzz.com/

---

## Project Overview

**Mivibzzz.com** provides a powerful website monitoring and alerting platform designed to help businesses, developers, and site owners maintain reliable, secure, and high-performance online services.

The Mivibzzz monitoring platform tracks **uptime, response times, SSL certificates, security headers, page changes, and domain expiration** for websites and APIs. Automated checks run continuously, delivering instant alerts and detailed analytics so issues can be detected and resolved before users are impacted.

---

## Technology Stack

| Category | Technology |
|--------|-----------|
| Framework | Flask 3.0.0 |
| Database | SQLite with SQLAlchemy 2.0.23 ORM |
| Background Jobs | APScheduler 3.10.4 with ThreadPoolExecutor |
| Payments | Stripe 7.8.0 |
| HTTP Client | Requests 2.31.0, HTTPX 0.26.0 |
| SSL / Crypto | Cryptography 41.0.7, PyOpenSSL 23.3.0 |
| DNS / Domain | dnspython 2.4.2, python-whois 0.8.0 |
| Email | Gmail SMTP |
| Frontend | Vanilla JavaScript, Chart.js |

---

## Uptime Monitoring

Mivibzzz provides continuous uptime monitoring to ensure your website or API remains online and responsive. Automated checks are performed at regular intervals, with immediate notifications sent when issues are detected—allowing you to respond before users are affected.

---

## How It Works

The monitoring process follows a simple and reliable workflow:

### 1. HTTP Requests
Scheduled HTTP GET requests are sent to your website or API.

### 2. Response Analysis
Responses are evaluated for connectivity, timeouts, and valid HTTP status codes (2xx).

### 3. Status Updates
Each monitored service is marked as **UP (green)** or **DOWN (red)** in the dashboard.

### 4. Instant Alerts
Email notifications are sent immediately when status changes occur.

### 5. Incident Logging
All downtime events are logged with timestamps for historical analysis and reporting.

---

## Understanding Uptime Percentages

Uptime represents the percentage of time your service is available during a given period.

| Uptime | Downtime / Month | Downtime / Year | Rating |
|------|-----------------|----------------|--------|
| 99.999% | 26 seconds | 5 minutes | Excellent |
| 99.99% | 4 minutes | 52 minutes | Excellent |
| 99.9% | 43 minutes | 8.7 hours | Good |
| 99% | 7.2 hours | 3.6 days | Fair |
| 95% | 36 hours | 18.2 days | Poor |

For most production websites and APIs, an uptime target of **99.9% or higher** is recommended. Mivibzzz automatically tracks uptime and provides clear visibility into availability and outages.

---

## Response Time Analytics

Mivibzzz response time analytics help ensure fast, reliable user experiences by tracking how quickly your server responds to requests. Performance slowdowns can be identified early, trends analyzed, and alerts triggered when thresholds are exceeded.

---

## What Is Response Time Monitoring?

Response time monitoring measures how quickly a server responds to incoming requests. While uptime confirms availability, response time reflects **performance quality**.

Mivibzzz measures **Time To First Byte (TTFB)** on every check, capturing the time from request initiation to the first byte received. This metric is a strong indicator of backend performance and processing speed.

Advanced analytics are available for Pro users, including historical trends, averages, percentiles, and response-time alerts.

---

## Key Features

- **Real-Time Tracking**  
  Response time measured on every check, with up to 1,440 data points per day at 1-minute intervals.

- **Trend Analysis**  
  Performance trends across 24 hours, 7 days, and 30 days.

- **Percentile Metrics**  
  95th percentile calculations highlight worst-case performance.

- **Performance Alerts**  
  Notifications when response times spike or remain above acceptable limits.

---

## Response Time Benchmarks

| Response Time | Rating | User Experience |
|--------------|--------|----------------|
| Under 100ms | Excellent | Feels instant |
| 100–200ms | Good | Fast and responsive |
| 200–500ms | Acceptable | Noticeable but tolerable |
| 500ms–1s | Slow | Users notice delay |
| Over 1 second | Poor | High bounce risk |

---

## Analytics Dashboard

The Mivibzzz analytics dashboard provides:

- Current response time
- Average response time over selected periods
- Minimum and maximum recorded times
- 95th percentile performance
- Visual trend charts
- Automatic anomaly detection

---

## Use Cases

- Performance optimization
- SLA compliance monitoring
- Capacity planning
- Third-party service impact assessment

---

## Why Response Time Matters

- **User Experience** – Faster sites reduce frustration and bounce rates  
- **SEO** – Page speed affects search engine rankings  
- **Conversions** – Faster load times improve conversion rates  

---

## SSL Certificate Monitoring

Mivibzzz continuously monitors SSL/TLS certificates to prevent unexpected expirations and security warnings. Alerts are sent well in advance so certificates can be renewed without disruption.

---

## What Is SSL Certificate Monitoring?

SSL monitoring checks certificate validity, expiration dates, issuers, and configuration. Expired certificates result in browser warnings that can immediately drive users away.

Mivibzzz sends email alerts **14+ days before expiration**, giving you time to renew safely.

---

## SSL Key Features

- Expiration tracking
- Early renewal alerts
- Issuer visibility
- Valid, expiring, expired, and error states

---

## SSL Certificate Status Levels

| Status | Days Remaining | Action |
|------|---------------|--------|
| Valid | More than 14 days | No action required |
| Expiring Soon | 14 days or less | Renew certificate |
| Expired | 0 or negative | Urgent action required |
| Error | N/A | Check configuration |

---

## Page Change Detection

Mivibzzz monitors your web pages for unexpected or unauthorized content changes such as defacements, injected scripts, or unplanned edits.

---

## How Page Change Detection Works

1. Page HTML is downloaded during each check  
2. A SHA256 hash is generated  
3. The hash is compared to the previous value  
4. Differences trigger a change event  
5. Alerts are sent for investigation  

---

## Detected Changes Include

- Text additions or removals  
- HTML structure changes  
- Link and URL updates  
- Image source changes  
- Script injections or modifications  
- Meta and SEO tag changes  

---

## Domain Expiry Monitoring

Mivibzzz monitors domain registration status, expiration dates, and DNS records to protect your online presence from accidental expiration or hijacking.

---

## What Is Domain Expiry Monitoring?

WHOIS databases are queried to retrieve expiration dates, registrar details, and domain metadata. Alerts are sent **30 days before expiration**.

DNS monitoring detects unexpected changes that may indicate misconfiguration or security issues.

---

## DNS Records Monitored

| Record | Purpose | Why Monitor |
|------|--------|-------------|
| A | IPv4 mapping | Detect IP changes or hijacking |
| AAAA | IPv6 mapping | Track IPv6 changes |
| CNAME | Aliases | Ensure CDN integrity |
| MX | Mail routing | Detect email failures |
| TXT | SPF / DKIM | Monitor email auth |
| NS | Nameservers | Detect DNS control changes |

---

## Security Headers Analysis

Mivibzzz analyzes HTTP security headers and provides actionable recommendations to protect against common web attacks.

---

## Headers Checked

- Strict-Transport-Security (HSTS)
- Content-Security-Policy (CSP)
- X-Frame-Options
- X-Content-Type-Options
- X-XSS-Protection
- Referrer-Policy
- Permissions-Policy

---

## Security Grades

| Grade | Score | Meaning |
|------|------|--------|
| A | 90–100% | Excellent |
| B | 80–89% | Good |
| C | 70–79% | Acceptable |
| D | 60–69% | Poor |
| F | Below 60% | Critical |

---

## Status Page Widget

Build trust by displaying real-time service status directly on your website.

### Embed Code

html
<script src="https://webmonitor.mivibzzz.com/static/js/embed.js"
        data-website-id="YOUR_WEBSITE_ID"
        data-theme="light"></script>

### Widget API

#### Endpoint

GET /api/widget/{website_id}


#### Response

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


CORS is enabled for cross-domain access.

Email Alerts & Notifications

Mivibzzz sends instant, reliable notifications without alert fatigue.

## Alert Types

🚨 Downtime alerts

✅ Recovery notifications

🔒 SSL expiration warnings

📋 Weekly performance digests

#### Alerts are sent once per incident start and once on recovery.

### Notification Configuration

Enable or disable alerts in account settings

Toggle weekly summary emails

Ensure alert emails are whitelisted
