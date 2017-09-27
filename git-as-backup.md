# GitHub as backup

Git is a "version control system". This means it helps you keep track of
different versions of your files. Instead of having lots of different files
named `report.doc` and `report_final.doc` and `report_final_v2.doc`, etc
you just have `report.doc`. To see older versions you use Git.

![versions](images/phd101212s.gif)

GitHub is a web-service that you can use to store a copy of your git repository.

The best way to get started using Git and GitHub is to treat it as a
cloud based backup.


## Getting started

First let's create an account on GitHub if you do not already have one. To sign
up visit: https://github.com/.

When we use Git on a new computer for the first time, we need to configure a
few things. On a command line, Git commands are written as `git verb`, where
`verb` is what we actually want to do. Here is how to setup your new laptop
(if your name is Dracula):
```
$ git config --global user.name "Vlad Dracula"
$ git config --global user.email "vlad@tran.sylvan.ia"
```
_Note: use the email address you used to sign up for GitHub._

The two commands we just ran above only need to be run once: the flag `--global`
tells Git to use the settings for every project, in your user account, on this
computer.

You can check your settings at any time:
```
$ git config --list
```

As you are working as a pair, take a moment to also create an account and setup
Git for the second member in your team on their laptop. After you are done with
that, close their laptop again.

---

🚧 Close the other laptop again. 🚧

---

## Creating your first repository

In a browser visit https://github.com/ and login. To create a new repository
find the big plus sign (+) in the upper right hand corner. Click it and select
"New repository". We will use "zuri-velo" as the name for the repository. If you
want to you can add a short sentence describing the repository. Make sure to
select "public" and not "private". Select "Initialize this repository with a README".
The last step is to click "Create repository".

_Note: if you are a student you can sign up for GitHub's "Student Developer Pack".
This will get you free, unlimited private repositories (while you are a student). Checkout https://education.github.com/ for more._

A detailed guide for creating a repository: https://help.github.com/articles/create-a-repo/

You can now look at your repository in your web browser. You should see the name,
the description and the README.


## Getting a copy of your repository on your laptop

To get a copy of your repository on your laptop you need to "clone" it. Use your
Git client to clone the repository:

```
# Clone your repository
git clone https://github.com/YOURNAME/zuri-velo
```
This will create a sub-directory called `zuri-velo`. In it you should find
the README file that you saw in your browser.


## Adding our notebook

We can now move the notebook we created to analyse the bike traffic in Zurich
into this repository. Once you have done that you can check the current state
of your repository by typing:
```
git status
```
This will inform you that there is one file which `git` does not know about
called `bikes-per-week.ipynb`.

You need to add it to the list of files `git` keeps track of with:
```
git add bikes-per-week.ipynb
```
Then check that the right thing happened:
```
git status
```
Git now knows that it’s supposed to keep track of `bikes-per-week.ipynb`, but
it has not recorded these changes as a commit yet. To get it to do that, we
need to run one more command:
```
git commit -m "Add first analysis of bikes per week"
```
When we run `git commit`, Git takes everything we have told it to save by using
`git add` and stores a copy permanently inside the special `.git` directory.
This permanent copy is called a `commit` (or `revision`) and its short
identifier is `f22b25e` (Your commit may have another identifier.)

We use the `-m` flag (for “message”) to record a short, descriptive, and
specific comment that will help us remember later on what we did and why. If we
just run `git commit` without the `-m` option, Git will launch nano (or whatever
other editor we configured as `core.editor`) so that we can write a longer
message.

Good commit messages start with a brief (<50 characters) summary of changes
made in the commit. If you want to go into more detail, add a blank line between
the summary line and your additional notes.

If we run git status now:
```
git status
```
it tells us everything is up to date.

If we want to know what we have done
recently, we can ask Git to show us the project’s history using `git log`:
```
git log
```
This will list all commits made in reverse chronological order. The listing for
each commit includes the commit's full identifier (which starts with the same
characters as the short identifier printed by the git commit command earlier),
the commit's author, when it was created, and the log message Git was given
when the commit was created.

Once your history starts getting too long you can limit how many messages you
want to see by running `git log -1` to see only the last commit. To see the
last two use `git log -2`, etc.


## Storing changes on GitHub

Git is a decentralized version control system. This means you can use it without
internet connection. This is extremely convenient for people who travel a lot.
However it does mean you need to remember to "push" your changes to GitHub in
order to have a backup. After making a commit you can copy your changes to
GitHub by running:
```
git push origin master
```
Visist your repository on GitHub and check that your changes have arrived.
