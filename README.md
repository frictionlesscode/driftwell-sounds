# driftwell-sounds

Ambient sound catalog for [Driftwell](https://github.com/frictionlesscode/affirmationApp).

Each release publishes a set of audio files plus a `manifest.json` describing them. The
Driftwell app fetches `manifest.json` from this repo's `latest` release alias, so the app
never needs a hardcoded-URL update as the catalog grows. Individual track URLs inside the
manifest point at their own tagged release asset (not `latest`), so they stay stable even
after `latest` moves on to a newer release.

## manifest.json schema

```json
{
  "sounds": [
    {
      "id": "string, stable identifier",
      "name": "string, display name",
      "category": "string, e.g. ambient / nature",
      "url": "direct URL to the release asset for this track",
      "sizeBytes": 0,
      "durationMs": 0,
      "sha256": "hex digest of the file, verified by the app before use",
      "license": "license under which the source file was obtained",
      "attribution": "attribution text, if the license calls for it"
    }
  ]
}
```

## License records

Keep a license/attribution record for every file, even for CC0/public-domain sources where
attribution isn't legally required. See each release's notes for source details.
