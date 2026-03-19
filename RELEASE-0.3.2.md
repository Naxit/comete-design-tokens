# @naxit/comete-design-tokens v0.3.2 — Première release

La fondation de l'écosystème Comète : un système de design tokens qui alimente l'ensemble des composants, icônes et interfaces du design system.

## Ce que contient cette release

Un fichier CSS unique (`comete-tokens.css`) qui expose l'intégralité des tokens sous forme de **CSS custom properties**, avec support natif du **light/dark mode** via l'attribut `data-theme`.

### Tokens primitifs

- **Couleurs** — 6 palettes complètes (biscay, lightning-yellow, red, salem, grey, porcelain) + couleurs de marque
- **Typographie** — Familles, tailles, line-heights, font-weights
- **Spacing & Sizing** — Échelle cohérente pour marges, paddings et dimensions
- **Border radius, Shadows, Z-index, Opacity**
- **Animation** — Durées et courbes d'easing standardisées
- **Breakpoints** — mobile, tablet, laptop, desktop

### Tokens sémantiques

- Tokens par composant (button, input, etc.) avec toutes les variantes de couleur, taille et spacing
- États interactifs : default, hovered, pressed, disabled, selected
- Tokens de surface : background, text, border, icon, blanket
- Déclinaison complète light + dark

## Stack technique

- **Source** : JSON au format Tokens Studio
- **Build** : Style Dictionary 5 + transforms Tokens Studio → CSS custom properties
- **Theming** : `:root` pour le light (défaut), `[data-theme="dark"]` pour le dark
- **Distribution** : GitHub Packages (`@naxit/comete-design-tokens`)

## Utilisation

```bash
pnpm add @naxit/comete-design-tokens
```

```css
@import "@naxit/comete-design-tokens/build/css/comete-tokens.css";
```

```css
.my-component {
  color: var(--text-default);
  background: var(--background-neutral-default);
}
```

## Écosystème

Ce package est une **peer dependency** de `@naxit/comete-design-system` et ses tokens de couleur d'icône (`--icon-*`) sont consommés par `@naxit/comete-icons`.
