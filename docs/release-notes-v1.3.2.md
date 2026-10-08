# DevArt Utils 1.3.2 — GitHub release draft

**Tag:** `v1.3.2`  
**Asset:** `pkg_devartutils_v1.3.2.zip`  
**SHA-256:** `0cc0ecd2977fa3205695a1d04c449f84c05d6020ebac7eca699c12e99800a30b`  
**Build path:** `builds/pkg_devartutils_v1.3.2.zip`

## Title

```
DevArt Utils 1.3.2 — Fix purge log user_id on upgrade
```

## Notes (GitHub body)

```markdown
## DevArt Utils 1.3.2

Maintenance release for Joomla 6 / PHP 8.3+.

**SHA-256:** `0cc0ecd2977fa3205695a1d04c449f84c05d6020ebac7eca699c12e99800a30b`

### Fixed

- Upgrade path now adds missing `#__devartutils_purge_log.user_id` for sites that created the table before that column existed (`CREATE TABLE IF NOT EXISTS` never altered older tables)
- Cloudflare host/URL purge success is no longer misreported as failure when only purge-history logging fails; schema is ensured at runtime with one retry

### Requirements

- Joomla 6.0+
- PHP 8.3+

### Update channel

After this asset is published, `update.xml` / `changelog.xml` on `main` point to this release. Upgrade path: **1.3.1 → 1.3.2** (also covers older installs missing `user_id`).
```
