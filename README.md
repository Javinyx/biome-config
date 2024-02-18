# @javinyx/biome-config

<p>
    <img alt="NPM Version" src="https://img.shields.io/npm/v/%40javinyx%2Fbiome-config?style=for-the-badge&logo=npm&logoColor=%23ffffff&labelColor=%23000000&color=%235a0873">
    <img alt="Libraries.io dependency status for specific release" src="https://img.shields.io/librariesio/release/npm/%40biomejs%2Fbiome/1.5.3?style=for-the-badge&logo=npm&logoColor=%23ffffff&label=%40biomejs%2Fbiome&labelColor=%23000000">
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
    "extends": ["./node_modules/@javinyx/biome-config/biome.json"],
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
      "editor.defaultFormatter": "biomejs.biome",
    },
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
        "quickfix.biome": "explicit",
        "source.organizeImports.biome": "explicit"
    }
    // ...
}
```
