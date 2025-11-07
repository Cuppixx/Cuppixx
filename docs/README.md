# Setup Guide

## Create PCA - Personal Access Token

1. Go to [github.com/settings/tokens](https://github.com/settings/tokens)
2. Click **Generate new token** >> **Generate new token (classic)**
3. Set **Note**: `METRICS_TOKEN`
4. Set **Expiration**: No expiration
5. Check scope: **`repo`** (Full control of repositories)
6. Click **Generate token**
7. **Copy the token** (starts with `ghp_...`) - you'll only see it once

## Add Token to Repository

1. Go to your profile repository **Settings**
2. Navigate to **Secrets and variables** >> **Actions**
3. Click **New repository secret**
4. **Name**: `METRICS_TOKEN` (must be exact)
5. **Secret**: Paste your token
6. Click **Add secret**

## Test the Workflow

1. Open the **Actions** tab and select the **Metrics** workflow
2. Click **Run workflow**
3. Wait for completion (~30-60 seconds)
4. Check that `metrics.plugin.languages.svg` appears in your repository

## Troubleshooting

- **Permission denied**: Verify token has `repo` scope and secret name is exactly `METRICS_TOKEN`
- **(no changes)**: Normal if your language stats haven't changed - make some code commits and try again
- **Image not showing**: Verify the SVG file exists and your README path is correct
