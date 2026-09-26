# Flask to GitHub Pages Example

A minimal demonstration of publishing the output of a dynamic Flask-style page as a static GitHub Pages site.

## How it works

The repository contains a generated `index.html` and a GitHub Actions workflow in `.github/workflows/static.yml`. GitHub Pages serves the static file; it does **not** run a Flask/Python server. Any dynamic Flask output must therefore be rendered to static HTML before deployment.

The workflow packages the repository's static content and deploys it through GitHub Pages whenever its configured trigger runs.

## Publishing

1. Enable GitHub Pages in the repository settings and select **GitHub Actions** as the source.
2. Push a change to the configured branch.
3. Check the Actions tab for the deployment result.

Open `index.html` directly to preview the current page locally.

## Key limitation

GitHub Pages only hosts static HTML, CSS, JavaScript, and assets. Server-side routes, databases, sessions, and other Flask runtime features require a separate hosting service.
