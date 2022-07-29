# VS Code Workspaces

Visual Studio Code pre-configured workspace collection of `.code-workspace` files.
The purpose of this repo is to facilitate VS Code _per repo_ settings/extensions.

- [VS Code Workspaces](#vs-code-workspaces)
  - [How to use](#how-to-use)
  - [Create a new](#create-a-new)
  - [Editing](#editing)
    - [Add recommended extension](#add-recommended-extension)
    - [Add settings](#add-settings)
      - [The file way](#the-file-way)
      - [The interface way](#the-interface-way)
    - [Example file](#example-file)

## How to use

1. Grab the `.code-workspace` file and opens it with VS Code
2. Go to `extensions` tab and filter by `recommended`
3. **Install** and use **Enable (Workspace)** option

## Create a new

Just use the `_.code-workspace` file as a template, rename it and open it with VS Code.

## Editing

### Add recommended extension

1. Go to extension tab and find the desired extension
2. Click on "config" icon
3. Click on `Add to Workspace Recommendations`
4. Select the option that is **DON'T** have `Workspace Folder` after its name

### Add settings

I'd prefer to go by the file way, but you can do it the way you want. Refer to [VS Code docs](https://code.visualstudio.com/docs/getstarted/settings) for more information.

#### The file way

Just open the `.code-workspace` file on editor and starts typing, VS Code will auto-complete variable names for you.

#### The interface way

You can go to VS Code settings tab and start changing settings on `Workspace` tab and it'll create settings inside `.vscode` directory, then you can copy and paste it inside the `.code-workspace` file.

### Example file

```jsonc
{
    "folders": [
        {
            "path": "."
        },
    ],
    "settings": {
        // Global setting
        "editor.defaultFormatter": "vscode.json-language-features",
        "editor.tabSize": 4,

        // File type specific setting
        "[jsonc]": {
            "editor.defaultFormatter": "vscode.json-language-features",
            "editor.tabSize": 4,
        },
    },
    "extensions": {
        "recommendations": [
            "donjayamanne.githistory",
        ]
    }
}
```
