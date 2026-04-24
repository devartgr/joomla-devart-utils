# DevArt Utils for Joomla

Advanced administrator toolkit for Joomla 6 with Cloudflare cache control, GA4 real-time insights, cache diagnostics, and productivity tools.

## Features

- Cloudflare cache purge integration
- Purge current site / subdomain cache
- Purge specific Cloudflare URL
- Joomla cache cleaning tools
- GA4 real-time dashboard
- Cache diagnostics
- Secure credential handling
- Encrypted storage for API secrets
- Joomla 6 administrator integration

## Included Extensions

This package installs:

- `com_devartutils`
- `plg_system_devartcache`
- `plg_system_devartcleancache`

## Requirements

- Joomla 6.x
- PHP 8.1+
- Cloudflare account (optional)
- Google Analytics 4 service credentials (optional)

## Security Highlights

- Cloudflare credentials stored securely
- CSRF protection for privileged actions
- Access control checks for administrative operations
- Safe API request handling

## Installation

1. Download latest package release
2. Go to Joomla Administrator
3. Extensions → Install
4. Upload package zip

## Cloudflare Setup

Recommended token permissions:

- Zone: Read
- Cache Purge: Edit
- Zone Analytics: Read (optional)

## Google Analytics Setup

Use a Google service account JSON file with access to your GA4 property.

## Version

Current stable release: **1.2.2**

## Author

Kostas Stathopoulos - DevArt

## License

GPL v3
