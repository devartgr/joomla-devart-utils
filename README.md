# DevArt Utils for Joomla

Advanced administrator toolkit for Joomla 6 with Cloudflare cache control, GA4 real-time insights, cache diagnostics, and productivity tools.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.1%2B-green)
![Release](https://img.shields.io/badge/Version-1.2.6-orange)
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

### Google Analytics 4
- Real-time visitor dashboard
- Property integration
- Secure credential storage

### Joomla Tools
- Joomla Page Cache detection
- Cache diagnostics
- Administrator quick actions
- Cache rules support
- Performance utilities

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

---

## Stability Improvements in 1.2.6

- Fixed Settings save inconsistencies introduced after recent hardening changes
- Fixed stale Yes / No toggle values after saving settings
- Fixed Cloudflare connection state mismatches on some installations
- Fixed System Check reporting missing token while encrypted credentials existed
- Fixed debug headers not always reflecting current saved settings
- Added hard exclusion for `/administrator` paths in the DevArt Cache plugin
- Improved parameter loading reliability across hardened and migrated sites
- TTL labels now clearly indicate values are measured in seconds

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

---

## Recommended Cloudflare Administrator Rule

For Joomla administrator areas, legacy Cloudflare Page Rules may still be useful:

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

**1.2.6**

---

## Changelog 1.2.6

- Fixed Settings save / stale toggle state issues
- Fixed Cloudflare token status inconsistencies
- Fixed debug header state reliability
- Added administrator hard exclusion in cache plugin
- Improved parameter loading consistency
- Improved TTL clarity (seconds)

---

## Author

**Kostas Stathopoulos**  
DevArt

---

## License

GPL v3
