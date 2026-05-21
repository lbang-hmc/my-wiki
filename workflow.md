# MkDocs Workflow Cheat Sheet

## Every session — activate the environment first
```bash
cd my-wiki
source venv/bin/activate
```

---

## Write & preview
```bash
mkdocs serve          # start local server at localhost:8000
# edit files in docs/ — browser auto-reloads on save
# Ctrl+C to stop the server
```

---

## Save & deploy
```bash
git add .
git commit -m "describe what you changed"
git push                  # saves source to GitHub
mkdocs gh-deploy          # builds & publishes to GitHub Pages
```

---

## Add a new page
1. Create a `.md` file in `docs/`, e.g. `docs/my-topic.md`
2. Add it to `mkdocs.yml` under `nav:` (optional — MkDocs will auto-detect it otherwise)

```yaml
nav:
  - Home: index.md
  - My Topic: my-topic.md
```

---

## Quick Markdown reference
```
# H1  ## H2  ### H3

**bold**   _italic_   `inline code`

- bullet item
1. numbered item

[link text](https://example.com)

![image alt](path/to/image.png)

| col1 | col2 |
|------|------|
| a    | b    |
```
