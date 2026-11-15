# Sound Machine firmware

Release files for the Sound Machine speakers (binaries only). Each speaker checks `latest.json` here about a minute
after joining Wi-Fi and every 6 hours; when the version is newer than its own, its web page shows an
**Update available** button that downloads and installs `firmware.bin` over HTTPS.

| File | What it is |
|---|---|
| `latest.json` | `{"version": "x.y.z", ...}` of the current release |
| `firmware.bin` | the ESP32-S3 application image for that version |

To release: replace `firmware.bin`, bump `version` in `latest.json`, commit both together.

## History
- **0.1.3** (2026-11-14): update button; volume 0-100 % on a loudness curve (50 % = -12 dB); look-ahead peak limiter instead of clipping (crackle fix); 80 ms audio buffer; Wi-Fi network search; `soundmachine-xxxx.local`; top ring shows the volume in its own colour.
