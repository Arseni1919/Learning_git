# Learning Git and GitHub

Some useful links.

- [Introduction to Git and GitHub for Python Developers | RealPython](https://realpython.com/python-git-github-intro/)
- [Create gitignore file | toptal.com](https://www.toptal.com/developers/gitignore)
- [A Guide to Git | blog](https://www.bobbywlindsey.com/2020/10/07/a-guide-to-git/)
- [Budges in GitHub README](https://shields.io/)
- [Getting started with GitHub Pages - 1](https://docs.github.com/en/pages/getting-started-with-github-pages)
- [Getting started with GitHub Pages - 2](https://pages.github.com/)
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)


# Introduction to Git and GitHub for Python Developers

### What Is Git?

Git is a distributed version control system (DVCS).

### Version Control
A version control system (VCS) is a set of tools that track the history of a set of files. This means that you can tell your VCS (Git, in our case) to save the state of your files at any point. Then, you may continue to edit the files and store that state as well. Saving the state is similar to creating a backup copy of your working directory. When using Git, we refer to this saving of state as making a commit.

### Distributed Version Control

OK, so that’s a version control system. What’s the distributed part? It’s probably easiest to answer that question by starting with a little history. Early version control systems worked by storing all of those commits locally on your hard drive. This collection of commits is called a repository. This solved the “I need to get back to where I was” problem but didn’t scale well for a team working on the same codebase.


## Basic Usage

```bash
$ git init
```

```bash
$ git status
```

## Adding a New File

```bash
$ git add hello.py
$ git status
```

## Committing Changes

```bash
$ git commit -m "creating hello.py"
[master (root-commit) 25b09b9] creating hello.py
 1 file changed, 3 insertions(+)
 create mode 100755 hello.py

$ git status
On branch master
nothing to commit, working directory clean
```

## Aside: The Staging Area

### .gitignore

```bash
# .gitignore
__pycache__
.idea
venv
env
.pytest_cache
.coverage
```

```bash
git commit -m "added myname module"

```

```bash
$ git add .gitignore
$ git commit -m "created .gitignore"
```

## Git Log

```bash
$ git log
```

## Going Back In Time: Checking Out a Particular Version of Your Code

...

## Working with Remote Repos

### Clone

```bash
git clone git@github.com:jima80525/github-playground.git
```

### Fetch

...

### Pull

```bash
git pull
```

### Push

```bash
git push origin [branch-name]
```

## Putting It All Together: Simple Git Workflow

1. `git status` – Make sure your current area is clean.
1. `git pull` – Get the latest version from the remote. This saves merging issues later.
1. Edit your files and make your changes. Remember to run your linter and do unit tests!
1. `git statu` – Find all files that are changed. Make sure to watch untracked files too!
1. `git add [files]` – Add the changed files to the staging area.
1. `git commit -m "message"` – Make your new commit.
1. `git push origin [branch-name]` – Push your changes up to the remote.


