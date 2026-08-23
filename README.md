# ops-cron

External scheduler for SkoobiLabs ops crons (`admin.skoobilabs.com`). Lives in its own **public** repo because GitHub Actions minutes are free and unlimited on public repos — the same schedules in a private repo burned the 2,000 free min/month in ~10 days (each curl-ping job bills a 1-minute minimum).

Nothing secret lives here: endpoint auth is the `CRON_SECRET` Actions secret. A failed run emails the repo owner — that's the dead-man's switch.

See `.github/workflows/ops-cron.yml` for the schedule and full history.
