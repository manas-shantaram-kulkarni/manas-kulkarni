# Manas Kulkarni Website

Personal website built with Jekyll.

## Edit Content

- Home page: `index.md`
- Education page: `education.md`
- Professional page: `professional.md`
- Timeline page: `timeline.md`
- Research entries: `_data/research.yml`
- Education entries: `_data/education.yml`
- Professional entries: `_data/experience.yml`
- Timeline entries: `_data/timeline.yml`
- Navigation: `_data/navigation.yml`

## Local Preview

Install dependencies once:

```sh
bundle config --local path vendor/bundle
bundle install
```

Build and watch for changes:

```sh
bundle exec jekyll build --watch
```

In another terminal, serve the generated site:

```sh
python3 -m http.server 4000 --bind 127.0.0.1 --directory _site
```

Open:

```txt
http://127.0.0.1:4000/
```
