# DevArt Utils 1.3.3 — GitHub release draft

**Tag:** `v1.3.3`  
**Asset:** `pkg_devartutils_v1.3.3.zip`  
**SHA-256:** `51bcb4c06e5a9b7b69f058a9ffa09687ecadc88a37c522890237866e990c7dcb`  
**Build path:** `builds/pkg_devartutils_v1.3.3.zip`

## Title

```
DevArt Utils 1.3.3 — Auto-clean for Events, Business, Video
```

## Notes (GitHub body)

```markdown
## DevArt Utils 1.3.3

Suite package for Joomla 6 / PHP 8.3+.

**SHA-256:** `51bcb4c06e5a9b7b69f058a9ffa09687ecadc88a37c522890237866e990c7dcb`

### Improved

- **Auto clean on content save** (same Settings toggle as articles) now also covers:
  - DevArt Events (`com_devartevents`)
  - DevArt Business (`com_devartbusiness`)
  - DevArt Video (`com_devartvideo`)
- On save / publish-unpublish-trash / delete: scoped Joomla cache clear + Cloudflare purge for item URL, listing, primary category, homepage, and configured extra URLs

### Fixed

- Auto-clean before-save / before-delete skip work when the setting is off
- Purge URL collection no longer mutates the live content item
- Per-request cache-clean coalesce documented as not a cross-request throttle

### Requirements

- Joomla 6.0+
- PHP 8.3+

### Update channel

After this asset is published, `update.xml` / `changelog.xml` on `main` point to this release. Upgrade path: **1.3.2 → 1.3.3**.
```
