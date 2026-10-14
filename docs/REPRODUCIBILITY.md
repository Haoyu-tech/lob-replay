# Reproduction guide

## View the bundled artifact

```powershell
python -m http.server 8000 --bind 127.0.0.1 --directory github_upload
```

Open `http://127.0.0.1:8000/lob-replay/` or the Chinese page at `/lob-replay/zh.html`.

Keep `index.html`, `zh.html` and `viz_data.js` together in the replay directory. The parent link expects the packaged homepage one directory up. See [README](../README.md) for file links.

## Validate

Check that the data script loads, replay controls and time selection work, and the language switch preserves valid navigation. The bundled data can be viewed without a new download.

## Regenerate

Raw MBO inputs, reconstruction/export scripts and a reference environment are not present. These are required to regenerate `viz_data.js` or change the recording. This cleanup documents and preserves the bundled sample; it does not validate original feed reconstruction.

## Run record

For every result you intend to compare or share, retain the repository commit, exact command/configuration, input-data identity, environment versions and output location. Save a dependency snapshot after a successful reference run; newly added requirements lists are intentionally unpinned until that validation exists.

## Validation status

Cleanup review: 14 October 2026. File paths and documented entry points were checked against the checkout. Full empirical results were not regenerated. Project-specific external prerequisites and known blockers are listed above.
