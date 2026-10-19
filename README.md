# aradhana-catalogue

The catalogue the Aradhana app downloads to get new bhajans, recordings and talks without an app update.

Release `db-<schema>` holds `aradhana-<version>.db` and the `manifest.json` naming it
(`{version, generatedAt, sha256, bytes, schema, url}`). The app checks
`releases/download/db-<schema>/manifest.json` every 6 hours, downloads a newer catalogue of its schema, verifies
its size and sha256, and opens it on its next launch.

Published by `pipeline/publish.sh` in AnoopamMission/aradhana-app; don't edit the release by hand.
