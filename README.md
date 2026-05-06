# DevArt Utils for Joomla 6

Advanced administrator toolkit for Joomla 6 with Cloudflare cache control, GA4 real-time insights, cache diagnostics, and performance tools for high-traffic websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.1%2B-green)
![Release](https://img.shields.io/badge/Version-1.2.10-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Official Documentation

📘 **User Manual (PDF)**  
[Download DevArt Utils Manual](docs/DevArt-Utils-Manual-v1.0.pdf)

---

## Features

### Cloudflare Tools
- Purge current site cache
- Purge Joomla + Cloudflare cache
- Purge specific Cloudflare URL
- Secure Connect / Disconnect workflow
- Cloudflare analytics support
- Cloudflare Cache Rules visibility
- Multi-site safe configuration handling

---

### Google Analytics 4
- Real-time visitor dashboard
- Property integration
- Secure credential storage

---

### Joomla Tools
- Deep Joomla cache cleaning (all cache layers)
- Joomla Page Cache detection
- Cache diagnostics
- Cache preview tools
- Administrator quick actions
- Cache rules support
- Performance utilities

---

### Performance Optimizations
- Optimized cache rule matching system
- Database indexing for faster rule lookups
- Reduced overhead for high-traffic environments
- Prepared groundwork for future rule caching optimizations

---

## Included Extensions

This package installs:

- `com_devartutils`
- `plg_system_devartcache`
- `plg_system_devartcleancache`

---

## Requirements

- Joomla 6.x
- PHP 8.1+
- Cloudflare account (optional)
- Google Analytics 4 credentials (optional)

---

## Security Highlights

- Encrypted server-side storage for credentials
- CSRF protection
- ACL checks for privileged actions
- Safe API request handling
- Clean uninstall / reinstall support
- GPL-compliant package and source structure

---

## 🚀 New in 1.2.10

### Administrator UI Improvements
- Added visual section headers across administrator pages
- Improved submenu page presentation and visual consistency
- Improved layout organization across Cache Rules, Diagnostics, Preview, Cloudflare and Settings pages
- Added Disclaimer / Limitation of Liability section in Settings

### Performance Improvements
- Added optimized database index for cache rules matching
- Improved scalability for large rule sets and high-traffic websites
- Reduced future overhead for cache rule processing

### Stability & Packaging
- Improved installer upgrade handling
- Improved package media asset handling
- Improved compatibility across Plesk and Virtualmin environments

---

## Previous Highlights

### 1.2.9 — JED Compliance & Licensing
- Added GPL license declarations in XML manifests
- Added GPL license headers in PHP files
- Prepared extension for Joomla Extensions Directory submission

### 1.2.8 — GitHub Update System
- Moved Joomla update server feed to GitHub
- Added GitHub Releases integration
- Improved update reliability behind Cloudflare

### 1.2.7 — Deep Cache Fix
- Fully clears Joomla cache (all cache groups)
- Fixes stale frontend content after updates
- Handles Page Cache / full HTML cache properly
- Improves cache reliability for production sites

---

## Screenshots

### Dashboard
![Dashboard](assets/screenshots/01.png)

### Cache Rules
![Cache Rules](assets/screenshots/02.png)

### Cache Diagnostics
![Diagnostics](assets/screenshots/03.png)

### Cache Preview
![Preview](assets/screenshots/04.png)

### Cloudflare Tools
![Cloudflare](assets/screenshots/05.png)

### GA4 Realtime
![GA4](assets/screenshots/06.png)

### Settings
![Settings](assets/screenshots/07.png)

---

## Installation

1. Download the latest release package
2. Open Joomla Administrator
3. Go to **System → Extensions → Install**
4. Upload the package zip file
5. Open **Components → DevArt Utils**
6. Configure your preferred settings

---

## Cloudflare Recommended Token Permissions

- Zone: Read
- Cache Purge: Edit
- Zone Analytics: Read (optional)
- Cache Rules: Read (optional)

---

## Recommended Cloudflare Administrator Rule

For Joomla administrator areas:

- `/administrator/*`
- Bypass Cache
- Disable Performance

---

## Google Analytics Setup

Use a Google service account JSON file with access to your GA4 property.

Then enter:

- Numeric GA4 Property ID
- Upload JSON credentials file

---

## Current Stable Version

**1.2.10**

---

## Author

**Kostas Stathopoulos**  
DevArt

---

## License

GNU General Public License v3 or later

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be held liable for any damages, data loss, downtime, security issues, or other problems resulting from the use or misuse of this software.

Users are responsible for testing the software in their own environment and maintaining proper backups before installation or upgrades.

Always test on a staging environment before using in production.
