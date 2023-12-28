# Compendium
Collection of my study notes on various topics.

Visit in GitHub Pages [here](https://hrstnikolov.github.io/compendium/intro.html).

Requireted python packages to build and deploy the book: `jupyter-book`, `ghp-import`.


| Action | Command |
|---|---|
| Build the jupyter book. If the table of contents is broken, add `--add` option to the command. | `jb build compendium` |
| Deploy book to GitHub Pages. | `ghp-import -n -p -f _build/html` |
| Save packages for future use. | `conda list --export > package-list.txt` |
| Reinstall packages from an export file. | `conda create -n myenv --file package-list.txt` |
| Freeze requirements and create requirements.txt. [^1] | `pip list --format=freeze > requirements.txt` |



[^1]: I do not know the correct way to freeze the requirements of a conda env. `conda list --export` did not find the packages installed using pip. The file produced by vanila `pip freeze` has strage format using the `@` character. This command above seems to be workaround. TODO investigate further.