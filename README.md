# bibtex-database
BiBTeX database

This repository contains a copy of the [BiBTeX database](https://www.iro.umontreal.ca/~lecuyer/tex-bibtex.html)
of Pierre L'Ecuyer, DIRO, Université de Montréal. It is used mainly to add BiBTeX references and citations 
in the documentation of software libraries produced by LaTeX, Doxygen, and similar tools. 

## How to use this BiBTeX database in your Git project?

This BiBTeX database is meant to be used as a [Git submodule](https://git-scm.com/docs/git-submodule). 

### To add it to your project

If you have a Git project in the repository `git/my_repo` and want to add the .bib files in the `doc/bib` subfolder, 
open a terminal in your local clone of `git/my_repo` and type:

```
git submodule add https://github.com/umontreal-simul/bibtex-database/ doc/bib
```

This will add the BiBTeX database as a submodule in doc/bib inside your repository. 
The .bib files will be in doc/bib/*.bib.
Note that Git commands are not 'recursive' and do not automatically apply to submodules, 
so if you want to clone your repository together with the submodule, you should use

```
git clone --recurse https://github.com/my_repo
```

so that the submodules are also cloned.

### Updating the version of the database

If you already have the database as a submodule and just want to update it to the latest version,
open a terminal in `git/my_repo` and type:

```
cd doc/bib
git pull
git status
cd ../..
git add doc/bib
git commit -m "update bibtex-database"
git push
```

You can find more details on Git submodules in the [Git documentation](https://git-scm.com/docs/).

### Updating this database itself

The latest version of this database is always maintained on Dropbox. To update files in this repository, 
it suffices to upload the new files using "add file -> upload files", assuming that you have the right to do so.



