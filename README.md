# bibtex-database
BiBTeX database

This repository contains the BiBTex database used by the Simulation and Optimization Laboratory from the DIRO at Universite de Montreal.

See the [website of Pierre L'Ecuyer](http://www.iro.umontreal.ca/~lecuyer/tex-bibtex.html) for details.

## How to use the BiBTex database in your project ?

The BiBTeX database is meant to be used as a [Git submodule](https://git-scm.com/docs/git-submodule). 
What follows mainly explain how to use this repository as a submodule in your project.

### Adding the database to your project
Say your project is contained in the repository `umontreal-simul/my_repo` and that you wan to add the bibliography in the `doc/bib` folder.

First, open a terminal in your local clone of `umontreal-simul/my_repo`. Then, type the following command:
```
git add submodule https://github.com/umontreal-simul/bibtex-database/ doc/bib
```
This command will clone the BiBTeX database inside your repository and add it a submodule. Your repository will now contain a submodule. This is important to remember as Git commands are not 'recursive' and do not automatically apply to the submodules.

For instance, when you want to clone your repository containing a submodule, you may want to use
```
git clone --recurse https://github.com/umontreal-simul/my_repo
```
so that the submodules are also cloned.

### Updating the version of the databse

Suppose you have already added the database as a submodule of your repository and that you want to replace your current version of the database with the last version.

First, open a terminal in your local clone of `umontreal-simul/my_repo`. Then, type the following commands:

```
cd docs/bib
git pull
git status
cd ../..
git add docs/bib
git commit -m "update bibtex-database"
git push
```

You can find additional details on Git submodules on the [Git documentation](https://git-scm.com/docs/).

