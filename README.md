# jsdate.wtf

The JavaScript Date quiz at <https://jsdate.wtf>.

## Development

The site is self-contained in `public/index.html`; no build is needed.
Preview it with `python3 -m http.server --directory public 8000`.

## Deployment

Deploy only `public/`. Keep repository-only files outside that directory.
On Laravel Cloud, use static serving with directory `public`, no build or start
command, and edge-cache purging on deployment.
