# style-dictionary

**Bac à sable pour expérimenter avec [Style Dictionary](https://amzn.github.io/style-dictionary/)** avant de l’intégrer au projet **Comète**.

## Objectif

Ce repo sert à tester la configuration, la transformation et l’export de tokens de design (couleurs, typographie, espaces, etc.) via Style Dictionary.

RM : la version gratuite du plugin Figma `Token Studio`est restreinte.

## Utilisation (package npm)

Le package est publié sous le nom `@aexae/design-tokens`.

```bash
pnpm add @aexae/design-tokens
```

### Import TypeScript

```ts
import { buttonTokens } from "@aexae/design-tokens";
```

### Import SCSS

Les fichiers SCSS générés sont publiés dans `build/scss/` et accessibles via des subpaths.

```scss
@use "@aexae/design-tokens/scss/button.light.scss";
@use "@aexae/design-tokens/scss/base.scss";
```

### Accès aux sources JSON

```ts
import lightTheme from "@aexae/design-tokens/tokens/theme/light.json";
```

## Commandes

```bash
# Installation des dépendances
pnpm i

# Build des tokens
pnpm build
```

## Structure du projet

- `tokens` : fichiers sources contenant les design tokens (au format JSON)
- `build/scss` : fichiers SCSS générés (variables)
- `dist/` : bundle TypeScript (ESM) + types

## Liens utiles

- 📘 [Style Dictionary – Documentation officielle](https://amzn.github.io/style-dictionary/#/)
