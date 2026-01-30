Mivibzzz WebMonitor

Online Monitoring & Alerts Platform

Live Service: https://webmonitor.mivibzzz.com/

Project Overview

Mivibzzz WebMonitor is the official website monitoring and alerting platform for Mivibzzz.com.
Formerly known as MerySpeak, the service has been fully integrated into the Mivibzzz ecosystem and now operates as its dedicated uptime, performance, and security monitoring solution.

WebMonitor provides real-time visibility into website availability, response times, SSL certificates, security headers, page integrity, and domain expiration—helping site owners detect issues early and maintain reliable, secure online services.

Relationship to MerySpeak

MerySpeak is now a product name / legacy service under the Mivibzzz brand

This repository is the canonical repo for Mivibzzz’s monitoring platform

webmonitor.mivibzzz.com is the primary production endpoint

MerySpeak.com will later be adjusted to reference this repo and service

Technology Stack
Category	Technology
Framework	Flask 3.0.0
Database	SQLite + SQLAlchemy 2.0.23
Background Jobs	APScheduler 3.10.4 (ThreadPoolExecutor)
Payments	Stripe 7.8.0
HTTP Clients	Requests 2.31.0, HTTPX 0.26.0
SSL / Crypto	Cryptography 41.0.7, PyOpenSSL 23.3.0
DNS / Domains	dnspython 2.4.2, python-whois 0.8.0
Email	Gmail SMTP
Frontend	Vanilla JavaScript, Chart.js
Core Features
✅ Uptime Monitoring

Continuous HTTP monitoring with instant alerts on downtime and recovery.

⏱ Response Time Analytics

Tracks Time To First Byte (TTFB) with trend analysis, percentiles, and performance alerts.

🔒 SSL Certificate Monitoring

Expiration tracking, issuer details, and early renewal warnings.

🧬 Page Change Detection

SHA256 hashing to detect defacements, injected scripts, or unauthorized content changes.

🌐 Domain Expiry & DNS Monitoring

WHOIS expiry tracking plus DNS record change detection (A, AAAA, CNAME, MX, TXT, NS).

🛡 Security Headers Analysis

Automated scoring and recommendations for modern HTTP security headers.

📊 Public Status Widget

Embeddable real-time uptime widget for transparency and trust.

📧 Alerting & Notifications

Downtime, recovery, SSL expiry, and weekly performance digests.

Status Widget (WebMonitor)
<script src="https://webmonitor.mivibzzz.com/static/js/embed.js"
        data-website-id="YOUR_WEBSITE_ID"
        data-theme="light"></script>

API – Status Widget

Endpoint

GET /api/widget/{website_id}


Response

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


CORS is enabled for cross-domain embedding.

Repository Purpose

This repository contains:

Core monitoring engine

Scheduler & background workers

Alerting and notification logic

API endpoints

Web dashboard frontend

Widget & public APIs

It is the authoritative codebase for Mivibzzz.com’s WebMonitor service.
