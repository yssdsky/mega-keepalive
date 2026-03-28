# MEGA Keepalive

Minimal GitHub Actions workflow for MEGA account keepalive.

## What it does

- Logs in to MEGA
- Lists `/`
- Uploads a tiny probe file
- Deletes the probe file

## Required GitHub Actions secrets

- `MEGA_EMAIL`
- `MEGA_PASSWORD`

## Run

- Push this repository to GitHub
- Add the two secrets in repository settings
- Open `Actions` and run `MEGA Keepalive`, or wait for the daily schedule
