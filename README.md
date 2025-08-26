# VisitGuide Desktop Updates

This repository hosts auto-update manifests and release files for the VisitGuide Desktop notification client.

## Purpose

This repository serves as the distribution point for:
- Update manifests (`latest.json`)
- Release binaries for the Windows desktop notification system
- Version history and SHA256 checksums

## How It Works

1. The desktop client checks `latest.json` for available updates
2. If a new version is available, it downloads from GitHub Releases
3. SHA256 verification ensures file integrity
4. Automatic rollback on update failure

## Manifest Structure

```json
{
  "latest": "1.4.3",
  "files": {
    "1.4.3": {
      "url": "https://github.com/visitguide-ai/visitguide-desktop-updates/releases/download/v1.4.3/staff_notifier-v1.4.3.exe",
      "sha256": "..."
    }
  }
}
```

## Important

This repository is automatically managed by CI/CD workflows. Manual changes should not be made to `latest.json`.

---

Part of the [VisitGuide](https://visitguide.ai) platform - One-stop communication hub for hotels.