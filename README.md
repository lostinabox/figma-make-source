# figma-make-source

> Source repository managed exclusively by **Figma Make**

## ⚠️ WICHTIG

Dieses Repo wird **komplett von Figma Make verwaltet**!

- ❌ Keine manuellen Edits hier
- ❌ Keine Pull Requests
- ❌ Keine direkten Commits

**Alles wird bei jedem Figma Make Push überschrieben!**

---

## 🏗️ Architektur

```
Figma Make → figma-make-source → GitHub Actions → actionpainting-design-system → npm
```

- **Repo A (hier):** [figma-make-source](https://github.com/lostinabox/figma-make-source)
  - Source of Truth
  - Verwaltet von Figma Make
  - Wird komplett bei jedem Push ersetzt

- **Repo B:** [actionpainting-design-system](https://github.com/lostinabox/actionpainting-design-system)
  - Release Repo
  - Mit GitHub Actions Workflow
  - Synct automatisch von diesem Repo
  - Published zu npm als `@actionpainting/design-system`

---

## 🔄 Workflow

1. **Du arbeitest in Figma Make**
2. **Push von Figma Make** → dieses Repo wird komplett ersetzt
3. **GitHub Actions** (in Repo B) erkennt Änderungen alle 10 Minuten
4. **Auto-Sync:** `src/` und `snippets/` werden kopiert
5. **Auto-Publish:** Version bump + npm publish

---

## 📦 NPM Package

Das fertige Package findest du hier:

```bash
npm install @actionpainting/design-system
```

**NPM:** https://www.npmjs.com/package/@actionpainting/design-system  
**Release Repo:** https://github.com/lostinabox/actionpainting-design-system

---

## 🎨 ActionPainting Branding

- **Farben:** Blau `#0000FF`, Rot `#EC0C00`
- **Font:** Questrial (Google Font)
- **Tone:** Herzlich, menschlich, klar, du-Ansprache
