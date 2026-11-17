# Desktop Copilot shared catalog

`index.json` lists the open-source tool recipes and flows that Desktop Copilot PCs share, and the ones that were
withdrawn. `index.json.sig` is its Ed25519 signature; the app uses the index only if the signature verifies.

A recipe is data, never code: which open-source release to fetch (pinned by the SHA-256 GitHub publishes) and which
command to run. To offer one, share it from the app; it is checked again before it is listed here.
