# DrumScript Web

<!--date_added:tues-10-nov-2026-->
<!--date_updated:fri-13-nov-2026-->

*In development*
>
Free browser-based drum transcription and tempo detection.
Powered by the [DrumScript](https://pypi.org/project/drumscript/)
Python package running in-browser via
[Pyodide](https://pyodide.org/).

## Features (v1)

- **Tempo Detection** -- estimate BPM from a drum audio file
- **Transcribe** -- generate PDF sheet music, JSON, and MIDI
  from an isolated drum stem

## How it works

1. You upload a WAV or MP3 drum stem in your browser.
2. Pyodide (Python compiled to WebAssembly) loads the real
   `drumscript` package from PyPI at runtime.
3. All processing happens locally -- nothing is uploaded to
   a server.

## Development

No build step. Open `index.html` in a browser (via a local
HTTP server for the Worker to load):

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Pushes to `main` auto-deploy to GitHub Pages via the
workflow in `.github/workflows/deploy.yml`.

## Licence

Apache-2.0 -- see [LICENSE](LICENSE).
