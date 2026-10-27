# traffick

Home of the **Local video player**: a single-file HTML video player (no install, no server) plus a small data trail of its versions and downloads.

## Get the player
Download `video-player.html` from the [latest release](../../releases/latest), then open it in Chrome, Edge, Firefox or Safari.

## How updates work
When you open Settings, the player asks the public GitHub API for this repo's latest release and compares the release tag (like `v1.6`) with its own version. It is a read-only request and sends no personal data. The player cannot replace itself, so if it says you are out of date, use the link to download the new file.

## Traffic data
- `traffic/stats.json`: latest snapshot with total downloads, downloads per version, and the latest version
- `traffic/history.csv`: one row per day (date, total downloads, latest version)
- Both are updated daily by `.github/workflows/stats.yml`, which you can also run by hand from the Actions tab.
- Numbers come from GitHub's download counter on release files. They count every download of the release file (not unique people) and do not include clones or views of the repo.

## Publishing a new version
1. Change `VERSION` in the player file.
2. Releases > Draft a new release > tag `vX.Y` > attach `video-player.html` > Publish release.
3. Add a short entry to `CHANGELOG.md`.
