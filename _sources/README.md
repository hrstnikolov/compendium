# Compendium
Collection of my study notes on various topics.

Requireted python packages to build and deploy the book: `jupyter-book`, `ghp-import`.


| Action | Command |
|---|---|
| build the jupyter book | `jb build compendium` |
| deploy book to GitHub Pages | `ghp-import -n -p -f _build/html` |
| save packages for future use | `conda list --export > package-list.txt` |
| reinstall packages from an export file | `conda create -n myenv --file package-list.txt` |
| freeze requirements [^1] | `pip list --format=freeze > requirements.txt` |



[^1]: I do not know the correct way to freeze the requirements of a conda env. `conda list --export` did not find the packages installed using pip. The file produced by vanila `pip freeze` has strage format using the `@` character. This command above seems to be workaround. TODO investigate further.