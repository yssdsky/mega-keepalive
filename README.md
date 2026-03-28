# MEGA Keepalive

Minimal GitHub Actions workflow for MEGA account keepalive.

## What it does

- Logs in to MEGA
- Lists `/`
- Uploads a tiny probe file
- Deletes the probe file
- Syncs source snapshots for:
  - `slotopol/server` -> `server-slots/latest.tar.gz`
  - `slotopol/bot` -> `bot/latest.tar.gz`
- Sends a failure email when SMTP secrets are configured

## Required GitHub Actions secrets

- `MEGA_EMAIL`
- `MEGA_PASSWORD`

## Optional GitHub Actions secrets

- `SMTP_SERVER`
- `SMTP_PORT`
- `SMTP_USERNAME`
- `SMTP_PASSWORD`
- `SMTP_TO`
- `SMTP_FROM`

## Optional GitHub Actions variables

- `MEGA_PATH`
  - default: `/`
- `MEGA_SYNC_ROOT`
  - default: `/source-sync`
  - if `MEGA_PATH` is not `/`, default becomes `<MEGA_PATH>/source-sync`

## Run

- Push this repository to GitHub
- Add the repository secrets in repository settings
- Open `Actions` and run `MEGA Keepalive`, or wait for the daily schedule
