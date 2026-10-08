# Changelog

## Template 1.1.0 — 2026-08-04

- Restored generic documentation placeholders for new product bootstrap.
- Added Joomla production-series and workspace awareness to `scripts/validate.php`.
- Added PHP minimum, compatibility targets, and extension checks to validation.
- Added stronger package and extension naming validation.
- Made `scripts/build.php` validation-first with a source integrity guard.
- Preserved the original simple template architecture.

Product change history for bootstrapped repositories begins below this template
section.

## 1.3.2 — 2026-10-08

### Fixed

- Upgrade path adds missing `#__devartutils_purge_log.user_id` for sites that created the table before that column existed (`CREATE TABLE IF NOT EXISTS` never altered it)
- Cloudflare host/URL purge success is no longer misreported as failure when only purge-history logging fails; schema is ensured at runtime with one retry

## 1.3.1 — 2026-10-07

### Security

- Migrate legacy plaintext Cloudflare API tokens into SecureStorage; AEAD (libsodium / AES-GCM) with per-install isolation
- Cache headers only for guest GET/HEAD HTML 200; logged-in always private no-store; fail-closed on rules/params load failure
- Preserve private/no-store and CDN private/no-store; form.token detection (including spaced attributes); Vary merge / Vary:* no-store
- Form-token scan runs last on `onAfterRender` and re-checks size-capped GZIP bodies when a later plugin injects a token form

### Fixed / Improved

- Newsroom auto-clean: save / state / delete purge article + previous URL + optional home/category; throttle; shared Cloudflare deadline and chunking
- Bulk purge no longer silently truncates article URLs (extras soft-capped; partial Cloudflare purge warned in admin)
- Cloudflare CDN SWR/SIE headers; logged-in + Remember Me bypass cookie docs; required Cloudflare Cache Rules in Settings
- Diagnostics edge-HIT-on-private warning; `Factory::getConfig` replaced with application config access
- Documented first-visit Set-Cookie cold-path limitation (T10) in Cloudflare setup guide

## 1.3.0 — 2026-10-07

### Added

- Suite package `pkg_devartutils` consolidating Utils, Administrator Tools, Favicon, Asset Repair, and related plugins
- Cache / Cloudflare / GA hubs; package-only update channel; 15-locale language packs
- Scheduled Cloudflare URL purge task plugin

### Changed

- First public suite release since 1.2.10 (intermediate 1.2.11–1.2.46 builds were not published)
- PHP 8.3+ / Joomla 6+ only; legacy `pkg_devartbackendtools` superseded

## 1.2.20 — 2026-08-24

### Changed

- Matched Cache and Cloudflare hub cards to Article Tools styling and improved responsive admin tables

## 1.2.19 — 2026-08-24

### Changed

- Refined Cloudflare hub button styling (Authors-style colors), removed Firewall Rules, and added Security Events plus Security Center Insights to Cloudflare Analytics

## 1.2.18 — 2026-08-24

### Changed

- Added Cloudflare admin submenu hub with Clear Cache, Cloudflare Analytics and Cloudflare Rules views, plus read-only Page Rules and Firewall rules

## 1.2.17 — 2026-08-24

### Changed

- Added Cache admin submenu hub with links to Cache Rules, Cache Diagnostics and Cache Preview, plus Back toolbar buttons on those views

## 1.2.16 — 2026-08-24

### Changed

- Added automatic Vary response headers for multilingual sites and logged-in cache mode to reduce incorrect edge language or session caching

## 1.2.15 — 2026-08-24

### Security

- Hardened debug response headers by stripping control characters from DevArt Cache diagnostic values
- Restricted Settings save POST handling to an explicit field allowlist

### Fixed

- Injected the Clean Cache toolbar script before the final closing body tag instead of replacing every body marker

## 1.2.14 — 2026-08-24

### Changed

- Cached enabled cache rules and component params in the frontend DevArt Cache plugin (1-minute TTL) with invalidation on rule and settings changes
- Preserved original query-string order and encoding when stripping tracking parameters for URL rule matching

## 1.2.13 — 2026-08-24

### Changed

- Added full administrator language packs for 15 locales across the component and system plugins
- Added repository i18n tooling to export, translate, validate, and build locale files with format-specifier protection

## 1.2.12 — 2026-08-24

### Security

- Hardened cache clean return URL handling to reject external open redirects
- Secured cache rules export with CSRF token validation and ACL checks
- Enforced ACL checks on cache rules import, delete, reorder, and selected export actions
- Restricted Google Analytics OAuth token requests to the official Google HTTPS endpoint
- Hardened filesystem cache cleanup to stay within allowed cache roots and skip symlink targets

### Fixed

- Reduced cache cleanup debug log exposure by logging relative cache paths instead of absolute filesystem paths

## 1.2.11 — 2026-08-24

### Security

- Secured the GA Realtime AJAX refresh endpoint with administrator client check, CSRF token validation, and ACL enforcement
- Fixed uninstall data retention so `keep_data_on_uninstall` is honored by the installer script

### Fixed

- Removed manifest uninstall SQL that always dropped DevArt Utils tables regardless of the keep-data setting
- Added `devartutils.garealtime` ACL action for granular GA Realtime access control

## 1.2.10 — 2026-05-04

### New

- Added visual section headers across DevArt Utils administrator pages
- Added Disclaimer / Limitation of Liability section in Settings
- Added optimized database index for cache rules matching

### Changed

- Improved administrator UI consistency across Cache Rules, Diagnostics, Preview, Cloudflare and Settings pages
- Improved submenu page presentation and visual organization
- Optimized cache rules database access for future scalability
- Improved installer upgrade handling for existing Joomla installations
- Improved media asset handling inside package installation
- Improved compatibility across Plesk and Virtualmin environments

### Performance

- Added optimized database index for faster rules lookup performance
- Reduced overhead for future large rule sets and high-traffic environments
- Prepared groundwork for additional cache rule optimizations in future versions

## 1.2.9

- Added GPL license declarations in all XML manifest files
- Added GPL license headers in all PHP files
- Ensured full compliance with Joomla Extensions Directory (JED) requirements
- Improved package structure and consistency for distribution

## 1.2.8

- Moved the Joomla update server feed to GitHub for more reliable extension updates
- Updated package metadata and manifests to use the GitHub-based update XML
- Prepared future DevArt Utils releases to be delivered directly from GitHub Releases

## 1.2.7

- Fixed incomplete Joomla cache clearing that caused frontend content to not update immediately
- Fixed DevArt Clean Cache not clearing all cache groups consistently across installations
- Fixed cases where Page Cache / full HTML cache remained active after purge actions
- Implemented deep Joomla cache cleaning covering all cache layers and cache groups
- Enhanced dashboard layout with top banner and improved structure

## 1.2.6

- Fixed administrator Settings save inconsistencies introduced after recent security hardening changes
- Fixed stale Yes / No toggle states being displayed after saving component settings
- Fixed Cloudflare connection status showing incorrect values on some installations
- Fixed System Check reporting Cloudflare token as missing while encrypted credentials existed
- Fixed debug headers state not always reflecting the currently saved configuration
- Fixed administrator cache conflicts by enforcing hard exclusion for /administrator paths in the DevArt Cache plugin
- Reworked internal parameter loading to improve consistency across Settings, Cloudflare, Diagnostics and plugins

## 1.2.5

- Fixed Cloudflare Cache Rules panel returning empty results after recent security hardening changes
- Fixed Cloudflare Cache Rules retrieval by restoring the correct Cloudflare cache settings endpoint
- Fixed Cloudflare rules visibility regression affecting previously working installations

## 1.2.4

- Fixed Joomla Page Cache plugin detection on Joomla 6 installations
- Fixed Cloudflare Zone Domain and Purge Scope Host values being overwritten by unrelated Settings saves
- Fixed Cloudflare configuration inconsistencies affecting some multi-site and migrated installations
- Fixed stale administrator form state after Cloudflare Connect / Disconnect actions
- Improved Cloudflare Connect workflow to reuse the stored encrypted token when updating zone or purge host values

Verification status belongs in `PROJECT_STATUS.md` and must record only
confirmed Joomla testing.
