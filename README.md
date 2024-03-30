# VSCode extensions and settings + other tools

That was me when I attempted to set up my VSCode environment for Python development for the first time. Check the boxes where you can relate:

- [ ] PyCharm is great but I miss VSCode lightness and customizability. Let's try to configure it.
- [ ] I have just configured VSCode for Python development but intellisense/autocomplete/suggestions are not working as expected.
- [ ] I have watched a lot of YouTube videos and read a lot of articles but it's still not working. I'm missing PyCharm...

If you can relate to any of the above, you are in the right place. I have been there and I have found a solution that works for me. I hope it works for you too.

> Disclaimer: I am not a professional developer. I am a Product Manager who codes. This guide is a result of my personal experience. It works for me and I hope it works for you too!

## Python related configuration (essential pack)

### 1 - Python Official extension
[![Python extension](img/python-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

```json
{
  "python.defaultInterpreterPath": "python3",
  "python.languageServer": "Pylance", // VERY IMPORTANT! Please recheck this setting after installing Pylance.
  "python.analysis.typeCheckingMode": "basic",
  "python.analysis.inlayHints.callArgumentNames": "all",
  "python.analysis.inlayHints.functionReturnTypes": true,
  "python.analysis.diagnosticMode": "workspace",
  "python.analysis.inlayHints.pytestParameters": true,
  "python.analysis.inlayHints.variableTypes": true,
  "python.analysis.completeFunctionParens": true,
  "python.analysis.indexing": true,
  "python.analysis.autoImportCompletions": true,
}
```

### 2 - Pylance Official extension
[![Pylance extension](img/pylance-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)

### 3 - Ruff: formatter for Python written in Rust ([link](https://github.com/astral-sh/ruff))

Benchmark results of Ruff against other formatters showed by the author:

![Ruff benchmark](img/ruff-benchmark.png)

I used to utilize `Pylint` alongside `black`, `isort`, and `flake8`, but I've swapped them out for ruff which re-implements the latter three in Rust (check the [FAQ](https://docs.astral.sh/ruff/faq/).)

### 4 - Ruff Official extension ([link](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff))
[![Ruff extension](img/ruff-vscode-extension.png)](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)
