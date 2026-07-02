# CV — Yuchi Shen

A responsive architecture-style academic CV generated with Jekyll and published through GitHub Pages.

Live site: <https://yuchishen.github.io/CV/>

## Edit content

All CV content lives in [`_data/cv`](./_data/cv). Each section has its own YAML file. Images and animated project previews are stored in [`assets`](./assets).

To update the website:

1. Edit the relevant YAML file locally or directly on GitHub.
2. Commit the change to the `main` branch.
3. Wait for the **pages build and deployment** workflow to finish (normally 1–2 minutes).
4. Refresh <https://yuchishen.github.io/CV/>. If an older version remains cached, use `Ctrl+F5` or append a new query string such as `?v=2`.

Keep existing field names and YAML indentation unless the page template is updated at the same time. Empty optional entries are not rendered where the template supports omission.

See [CONTENT_GUIDE.md](./CONTENT_GUIDE.md) for field definitions and examples.

## Local preview

Install Ruby with DevKit and Bundler, then run from the repository root:

```powershell
bundle install
bundle exec jekyll serve
```

Open <http://localhost:4000/CV/>. Changes to YAML files are regenerated automatically while the server is running.

A plain `python -m http.server` preview will not process Jekyll data or Liquid templates.

## Live site

- Website: <https://yuchishen.github.io/CV/>
- Repository: <https://github.com/YuchiSHEN/CV>
