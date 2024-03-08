# @javinyx/biome-config

<p>
    <img alt="NPM Version" src="https://img.shields.io/npm/v/%40javinyx%2Fbiome-config?style=for-the-badge&logo=npm&logoColor=%23ffffff&labelColor=%23000000&color=%235a0873">
    <img alt="NPM dev or peer Dependency Version" src="https://img.shields.io/npm/dependency-version/%40javinyx%2Fbiome-config/peer/%40biomejs%2Fbiome?style=for-the-badge&logo=dependabot&logoColor=ffffff&labelColor=000000">
</p>

## Usage

### Installation

```bash
npm|yarn|pnpm|bun add -D @biomejs/biome @javinyx/biome-config
```

Add the `extends` array to your project's `biome.json` file:

```jsonc
// <project-root>/biome.json
{
    "$schema": "./node_modules/@biomejs/biome/configuration_schema.json",
    "extends": "@javinyx/biome-config",
    // ...
}
```

Add scripts to your `package.json` if you haven't already:

```jsonc
// <project-root>/package.json
{
    //...
    "scripts": {
        "lint": "biome lint .",
        "lint:fix": "biome lint . --apply"
    }
    // ...
}
```

### Visual Studio Code Setup

1. Install the [BiomeJS Visual Studio Code extension](https://marketplace.visualstudio.com/items?itemName=biomejs.biome) if you haven't already.

2. Add the following settings to your project's `.vscode/settings.json`, or create them anew:

```jsonc
// <project-root>/.vscode/settings.json
{
    // ...
    "[javascript][javascriptreact][typescript][typescriptreact][json][jsonc]": {
      "editor.defaultFormatter": "biomejs.biome"
    },
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "quickfix.biome": "explicit",
        "source.organizeImports.biome": "explicit"
    }
    // ...
}
```
