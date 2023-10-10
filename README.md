# ctuthesis

This repository is a fork of https://github.com/tohecz/ctuthesis. Most of the original files are present, but the folder structure is cleaner to work with. It's designed to work well with Visual Studio Code and a LaTeX workshop extension.

# 1. Installation

## 1.1 Prerequisites

- [**VSCode LaTeX workshop**](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
- [**TexLive distribution**](https://tug.org/texlive/)

> [!NOTE]
> MacOS users: Make sure you have `latexindent` installed on your machine. Otherwise, LaTeX workshop may have trouble formatting your sources.

## 1.2 Usage

1. Make sure you have all the [**prerequisites**](#11-prerequisites)
2. Open the [**workspace file**](./.vscode/thesis.code-workspace) using Visual Studio Code
3. Open `thesis.tex` (your root file, this should include all the other `*.tex` files)
4. Make your changes and hit save
5. `.build` folder should be generated in the root of the workspace with bunch of intermediate files and a final [**pdf**](./.build/thesis.pdf)[^1].
6. Check out the original [**manual**](./manual.pdf) if you want to customize the thesis to your liking
7. Have fun writing your awesome thesis!

### 1.2.1 TODOs

To make your life a little bit easier, there are several `TODO: ` comments placed across the `*.tex` files to let you know that you should change their content before submitting your work.

# 2. Structure

```ini
✨ ctuthesis/ # Workspace root
├─ .build/ # Build directory (not in VCS)
│  ├─ thesis.pdf
├─ src/ # Source directory
│  ├─ assets/ # Asset directory, mainly CTU logo and font
│  │  ├─ ctu_logo_black.pdf
│  ├─ common/ # (almost) original ctuthesis *.tex files
│  │  ├─ ctuth-core.tex
│  │  ├─ ctuth-names.tex
│  │  ├─ ctuth-templates.tex
│  │  ├─ ctuth-pkg.tex
│  ├─ documents/ # Directory for all sorts of documents
│  │  ├─ zadani.pdf # Specification of your thesis
│  ├─ ctuthesis.cls # LaTeX class file that makes all the magic, don't worry about it too much.
│  ├─ ctuthesis.ist
│  ├─ thesis.tex # Entry tex file for your thesis
├─ manual.pdf # Original ctuthesis manual
```

# 3. N2H

- [ ] Technica font

[^1]: Files under `.build` folder are not committed to the version control system.
