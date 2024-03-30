# VSCode extensions and settings + other tools

That was me when I attempted to set up my VSCode environment for Python development for the first time. Check the boxes where you can relate:

- [ ] PyCharm is great but I miss VSCode lightness and customizability. Let's try to configure it.
- [ ] I have just configured VSCode for Python development but intellisense/autocomplete/suggestions are not working as expected.
- [ ] I have watched a lot of YouTube videos and read a lot of articles but it's still not working. I'm missing PyCharm...

If you can relate to any of the above, you are in the right place! I have found a solution that works for me. I hope it works for you too.

> Disclaimer 1: I won't be covering the installation of Python or VSCode. I assume you have them installed 👌

> Disclaimer 2: Let's make it simple and suppose Docker doesn't exist for now 😇

> Disclaimer 3: I am not a professional developer. I am a Product Manager who codes. This guide is a result of my personal experience. It works for me and I hope it works for you too! 🤜🤛

## Python related configuration (essential pack)

### 1 - VSCode editor settings to format on save: 

By default, to open the settings file, press `Ctrl + P` (or `cmd + P` on macOS) and type `Open User Settings (JSON)`. Then, paste the following settings:

```json
"editor.formatOnSave": true,
"editor.formatOnSaveMode": "file",
"editor.codeActionsOnSave": {
  "source.organizeImports": "explicit"
},
```

### 2 - Python Official extension
[![Python extension](img/python-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

```json
"python.defaultInterpreterPath": "python3",
"python.languageServer": "Pylance", // VERY IMPORTANT! Please recheck this setting after installing Pylance.
"python.analysis.typeCheckingMode": "basic",
"python.analysis.diagnosticMode": "workspace",
"python.analysis.completeFunctionParens": true, // I regretted not enabling this setting earlier...
"python.analysis.indexing": true,
"python.analysis.autoImportCompletions": true
```

### 3 - Pylance Official extension

Pylance is a language server for Python developed by Microsoft that provides a good experience for my Python development in VSCode when I work on FastAPI projects.

[![Pylance extension](img/pylance-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)

### 4 - Ruff: formatter for Python written in Rust ([link](https://github.com/astral-sh/ruff))

Benchmark results of Ruff against other formatters showed by the author:

![Ruff benchmark](img/ruff-benchmark.png)

I used to utilize `Pylint` alongside `black`, `isort`, and `flake8`, but I've swapped them out for ruff which re-implements the latter three in Rust (check the [FAQ](https://docs.astral.sh/ruff/faq/) for more details).

### 5 - Ruff Official extension ([link](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff))
[![Ruff extension](img/ruff-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)
