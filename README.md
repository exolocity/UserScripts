# UserScripts
Userscripts synced via greasy fork

## GitHub sync URL format for Greasy Fork

Use the **Raw** GitHub file URL as the sync URL. Greasy Fork accepts these formats:

- `https://raw.githubusercontent.com/YourOwnerName/YourProjectName/YourBranchName/path/to/script.user.js`
- `https://raw.githubusercontent.com/YourOwnerName/YourProjectName/refs/heads/YourBranchName/path/to/script.user.js`
- `https://github.com/YourOwnerName/YourProjectName/raw/YourBranchName/path/to/script.user.js`
- `https://github.com/YourOwnerName/YourProjectName/raw/refs/heads/YourBranchName/path/to/script.user.js`
- `https://github.com/YourOwnerName/YourProjectName/releases/latest/download/script.user.js` (release events only, where `script.user.js` is uploaded as a release asset)

## GitHub webhook setup for Greasy Fork

In your GitHub repository, go to **Settings → Webhooks → Add webhook** and set:

- **Payload URL:** `https://greasyfork.org/en/users/1051947-exolocity/webhook` (replace with your own Greasy Fork user webhook URL if using a different account)
- **Content type:** `application/json`
- **Secret:** (set your webhook secret; keep it private and never commit it to the repository)
- **Active:** checked

### Event selection

- To update Greasy Fork on all pushes, choose **Just the push event**.
- To update only on releases, choose **Let me select individual events**, uncheck **Pushes**, and check **Releases**.

Greasy Fork will look for modified files in either event type.
