# UserScripts
Userscripts synced via greasy fork

## Greasy Fork Sync Setup

Userscripts in this repository are automatically synced to Greasy Fork via a GitHub webhook. Each script includes `@updateURL` and `@downloadURL` metadata pointing to the raw GitHub file URL.

### Sync URL Format

The sync URL uses the GitHub raw file format:

```
https://raw.githubusercontent.com/exolocity/UserScripts/main/script-name.user.js
```

### GitHub Webhook Configuration

To enable automatic syncing, add the following webhook to this repository under **Settings → Webhooks → Add webhook**:

| Field | Value |
|---|---|
| Payload URL | `https://greasyfork.org/en/users/1051947-exolocity/webhook` |
| Content type | `application/json` |
| Secret | *(leave blank)* |

**Which events would you like to trigger this webhook?**
- To update Greasy Fork on all pushes: choose **Just the push event**
- To update Greasy Fork only on releases: choose **Let me select individual events**, uncheck **Pushes**, and check **Releases**

Ensure **Active** is checked.
