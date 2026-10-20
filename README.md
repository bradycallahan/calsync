# calsync

calsync is a personal, self-hosted calendar sync job. It keeps my Google Calendar and iCloud Calendar in step by **recreating events** on each side, rather than sharing or subscribing one calendar to the other.

It is built for one user (me) and is not a public service. There is nothing to sign up for.

## How it works

- Runs as a single Docker container on my own home server.
- Uses [vdirsyncer](https://github.com/pimutils/vdirsyncer) to talk to:
  - **Google Calendar**, over Google's CalDAV API with OAuth 2.0
  - **iCloud Calendar**, over Apple's CalDAV endpoint with an app-specific password
- Each selected calendar is paired with a twin of the same name on the other service. New, changed and deleted events sync both ways every 15 minutes.
- Sync state and credentials are stored only on my server.

## Google API access

calsync requests access to Google Calendar so it can read and write events in my own calendars. It is used only with my own Google account.

See [PRIVACY.md](PRIVACY.md) for how data is handled.

## Contact

Brady Callahan — bradycallahan04@gmail.com
