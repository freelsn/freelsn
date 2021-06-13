---
title: VS Code
---

```bash

{
    // vscode general settings
    "editor.detectIndentation": true,
    "editor.insertSpaces": true,
    // "editor.fontFamily": "Hack",
    "editor.fontLigatures": true,
    "editor.fontSize": 14,
    "editor.minimap.enabled": false,
    "editor.rulers": [72, 80],
    "editor.tabSize": 4,
    "editor.wordWrap": "on",
    "files.insertFinalNewline": true,
    // "files.trimTrailingWhitespace": true,
    "workbench.colorTheme": "Monokai",
    "explorer.confirmDragAndDrop": false,

    // only for python language files
    "[python]": {
        "editor.rulers": [72, 80],
        "editor.tabSize": 4,
        "editor.insertSpaces": true
    },
    // python vscode extension
    "python.pythonPath": "/bigdata/snliu/tutorials/cs230-code-examples/pytorch/vision/.env/bin/python",
    "python.linting.enabled": true,
    "python.linting.lintOnSave": true,
    "python.linting.pylintEnabled": true,
    // "python.linting.flake8Enabled": true,
    // "python.linting.pycodestyleEnabled": true,
    // "python.formatting.provider": "yapf",
    "python.terminal.activateEnvironment": false,
    "[yaml]": {
        "editor.tabSize": 2,
        "editor.insertSpaces": true
    },
    "python.linting.flake8Args": [
        "--max-line-length=120",
        "--ignore=E501,F405",
    ],
    "python.linting.pycodestyleArgs": [
        "--ignore=E501",
    ],
    "window.zoomLevel": 0,
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
    "terminal.integrated.shell.linux": "/bin/csh",
    "git.ignoreLegacyWarning": true,
    "[makefile]": {
        "editor.insertSpaces": false
    },
    "[html]": {
        "editor.tabSize": 2
    },
    "[javascript]": {
        "editor.tabSize": 2
    },
    "[php]": {
        "editor.tabSize": 2
    },
    "update.enableWindowsBackgroundUpdates": false,
    "update.mode": "none",
    "remote.SSH.configFile": "C:\\Users\\snliu\\.ssh\\config",
    "remote.SSH.useLocalServer": false,
    "workbench.activityBar.visible": true,
    "breadcrumbs.enabled": true,
    "files.associations": {
        "*.cgf": "json",
        "*.cfg": "json",
        "*.pyx": "python"
    },
    "editor.accessibilitySupport": "off",
    "[css]": {
        "editor.tabSize": 2
    },
    "files.trimTrailingWhitespace": true,
    "files.trimFinalNewlines": true,
}
```