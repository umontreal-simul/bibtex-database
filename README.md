# bibtex-database
BiBTeX database

This repository contains a copy of the BiBTeX database of the Simulation and Optimization Laboratory at the DIRO, Université de Montréal. See [HERE](http://www.iro.umontreal.ca/~lecuyer/tex-bibtex.html) for details.

## How to use this BiBTeX database in your project?

This BiBTeX database is meant to be used as a [Git submodule](https://git-scm.com/docs/git-submodule). What follows explains how to use it in your project.

### Adding the database to your project
Say your project is contained in the repository `umontreal-simul/my_repo` and that you wan to add the bibliography in the `doc/bib` folder.

First, open a terminal in your local clone of `umontreal-simul/my_repo`. Then, type the command:

```
git add submodule https://github.com/umontreal-simul/bibtex-database/ doc/bib
```

This will clone the BiBTeX database inside your repository and add it a submodule. Note that Git commands are not 'recursive' and do not automatically apply to submodules. So if you want to clone your repository containing a submodule, you may want to use

```
git clone --recurse https://github.com/umontreal-simul/my_repo
```

so that the submodules are also cloned.

### Updating the version of the database

If you have already added the database as a submodule of your repository and you want to replace your current version of the database with the last one, open a terminal in your local clone of `umontreal-simul/my_repo`, then type the following commands:

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

