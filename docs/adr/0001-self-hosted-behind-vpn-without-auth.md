# Self-hosted on a VPS behind a VPN, with Postgres and no login

Vagtplanen is a single-user tool. It runs as one Docker container on the owner's VPS and is reachable only through the owner's VPN. It stores its data in the owner's existing Postgres container, which it reaches over a shared Docker network. The app has no authentication because the VPN is the access control. That keeps a learning project free of auth work while still letting the owner use it from both phone and laptop.

## Considered Options

- **Local-first in the browser (IndexedDB)**: rejected. Data would be stuck on one device and lost if browser storage is cleared.
- **SQLite on the server**: technically enough for one person's data. Postgres was chosen because a Postgres instance already runs on the VPS, `timestamptz` handles Shifts that cross midnight and DST cleanly, and the owner wants to learn it.

## Consequences

- The server must never be exposed outside the VPN. Exposing it publicly (or adding a second user) means adding authentication first.
- The Postgres instance is not backed up. Losing the data is an accepted risk.
