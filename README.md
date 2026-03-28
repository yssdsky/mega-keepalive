# Automation Workflows

Minimal GitHub Actions workflows for MEGA keepalive and fork sync.

## Workflows

### MEGA Keepalive
- Logs in to MEGA
- Lists `/`
- Uploads a tiny probe file
- Deletes the probe file
- Sends a failure email when SMTP secrets are configured

### Sync Forks
- Syncs `yssdsky/server-slots` with `slotopol/server`
- Syncs `yssdsky/bot` with `slotopol/bot`
- Sends a failure email when SMTP secrets are configured

## Required secrets

### For MEGA Keepalive
- `MEGA_EMAIL`
- `MEGA_PASSWORD`

### For Sync Forks
- `FORK_SYNC_TOKEN`
  - should be a GitHub PAT that can update `yssdsky/server-slots` and `yssdsky/bot`

## Optional secrets

- `SMTP_SERVER`
- `SMTP_PORT`
- `SMTP_USERNAME`
- `SMTP_PASSWORD`
- `SMTP_TO`
- `SMTP_FROM`

## Optional variables

- `MEGA_PATH`
  - default: `/`

## Run

- Push this repository to GitHub
- Add the repository secrets in repository settings
- Open `Actions` and run either workflow manually, or wait for the daily schedules
