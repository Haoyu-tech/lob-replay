# Limit Order Book Replay

[Reproduction guide](docs/REPRODUCIBILITY.md) · [Code and artifact map](docs/REPOSITORY_MAP.md)

Static browser visualization of a recorded order-book sample. The English page identifies the sample as CME GLBX.MDP3, BTC.c.0, MBO, 2026-09-15 00:00–01:00 UTC.

## Repository map

| Path | Purpose |
|---|---|
| [github_upload/index.html](github_upload/index.html) | Packaged personal homepage |
| [github_upload/lob-replay/index.html](github_upload/lob-replay/index.html) | English replay |
| [github_upload/lob-replay/zh.html](github_upload/lob-replay/zh.html) | Chinese replay |
| [github_upload/lob-replay/viz_data.js](github_upload/lob-replay/viz_data.js) | Prebuilt visualization data |
| [github_upload/lob-replay/preview.png](github_upload/lob-replay/preview.png) | Preview image |

## Local preview

```powershell
python -m http.server 8000 --bind 127.0.0.1 --directory github_upload
```

Open `http://127.0.0.1:8000/lob-replay/` or `http://127.0.0.1:8000/lob-replay/zh.html`. No compilation or package installation is needed.

Serve or publish the whole `github_upload/` directory to retain relative links and the adjacent `viz_data.js`. The root of this repository contains no `index.html`; deploying it unchanged as a site root will not produce the intended homepage.

## Reproduction boundary

This repository provides a prebuilt replay, not the original MBO acquisition, reconstruction or data-export pipeline. Viewing the bundled sample is separate from regenerating it from raw feed data. The export code, original inputs and reference environment must be supplied for that workflow.

See [the reproduction guide](docs/REPRODUCIBILITY.md).
