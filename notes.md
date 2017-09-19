
## Welcome 10
what will happen now?

## form pairs 10
stand at the front if new to git, back if know git, then split
left right on python skill

## setup a virtualenv/conda env 5
```
$ conda create -n epfl-osip python pandas jupyter matplotlib
$ source activate epfl-osip
```

## get data 5
To make things more concrete we will use some real data: Velo Zaehlung in Zuri

https://data.stadt-zuerich.ch/dataset/verkehrszaehlungen-werte-fussgaenger-velo


## make a notebook 15
Study the number of riders going past Mythenquai in Zurich over the year. Can
we find some interesting trends?
```
$ jupyter notebook
```
plot data, select one station (ECO09113499) mythenquai, resample weekly,
show in and out traffic.

make the notebook linear.


## GitHub as cloud backup 15
introduce GitHub, make a new repo, add gitignore, license, name it.

setup git with username, email: http://swcarpentry.github.io/git-novice/02-setup/

clone repo locally, add our notebook, git commit, git push. Show it arrives
on GitHub. `git status`, what about the data? Add our data file to .gitignore.
`git commit, push` -> GitHub.

Why `git add`? Explain staging area, prepare what you want to commit.

https://try.github.io/levels/1/challenges/1

http://swcarpentry.github.io/git-novice/04-changes/


## README 25
Update the readme with something useful. Discussion: what should be in a README?

https://docs.google.com/presentation/d/19yIld1etX0kzRY3PqjbymVzCi2lyW90i44jLmHeoGPw/edit#slide=id.gef2e83792_0_15

* What are you doing? For who and why?
* How do I use this?
* How can I get involved? Or is this just a companion repository?
* How can I cite this?
* Where to find the examples?

Create a short README for your PhD project, something in your lab, an event,
or the Velo project we have been using.

https://mozillascience.github.io/WOW-2017/readme/

Upgoer5, can you write a project description upgoer5 style?
`git add, commit, push` your README

Some README examples:
* a template, maybe a bit long? https://github.com/RichardLitt/standard-readme
* a template https://gist.github.com/PurpleBooth/109311bb0361f32d87a2


## create a function to download data 10
make a reusable function for downloading the data, check if we already have it,
use case: other years (2016, 2017, etc)

---

## COFFEE!
3.30 talk on IP
4.00 coffee break we restart at 4.30pm

---

## move code to a python package 10
Now we want to create a second notebook that looks at week vs weekend days.

Problem: how do we reuse the download function? Move our function to a module!

Create a second notebook that looks at weekend vs week days. Using code from
our module.


## Testing stuff 5+5
Completely natural for us as scientists to test things. New tool in the lab,
new function, ... what is the equivalent of this for code?

http://katyhuff.github.io/python-testing/01-basics/

XXX add a function that computes something from our data: the mean of a bunch
of numbers. use in groupby()?

## test the `mean` function 10+10
`assert`, unittests, pytest

http://katyhuff.github.io/python-testing/02-assertions/
http://katyhuff.github.io/python-testing/04-units/
http://katyhuff.github.io/python-testing/05-pytest/


## Testing philosophy 10
What to test and how? Lots of simple/dumb tests will get you a very long way.
Do not try and be clever with your tests, usually not worth it.
http://katyhuff.github.io/python-testing/06-edges/


## Robots! 10
Use a robot to run your tests for you. Use travis, easy to setup.
http://katyhuff.github.io/python-testing/08-ci/
push some changes that break travis, how to check the status? Integrate the
badge in your README


## ROADMAP 25
https://docs.google.com/presentation/d/1ivuXSBp-fSk8qt9lmCmngn6Ymnc3AO1_t7ClWUgVuZI/edit
You don't know where you are going, making a plan will help you get there!


## CONTRIBUTING.md 10
How can others contribute to this? Write down things that you expect people to
do, what they should expect from you, what are the mechaniques of contributing?


## The style police 5
Just do it. `flake8` in action, other languages have other linters. Just use
them.


## Collaborating on GitHub 25
Fork, pull request, merge.


## jupyter for examples 10
jupyter notebooks are good for exploring ideas and as examples. Don't put
too much code into them.


## LICENSE 5
BSD, what else?


## Getting cited 10
zenodo for DOIs for code. Examples of bibtex in the README to tell people
about a paper they should cite for this work.

How to make your code citable and get academic credit for your wonderful work!:
1) Read here to learn how to automatically mint DOI's (data type) for releases https://guides.github.com/activities/citable-code/
These are data DOI's that allow people to cite your code. However these do not carry the same academic credit as paper DOI's.
2) Next you can use the Journal of Open Source Software joss.theoj.org and submit your code there. Following peer review and acceptance (you need to prepare a short paper.md file which should take <1h) of the work JOSS will mint a Crossref DOI.
JOSS is an actual academic journal with an ISSN, will (almost there) be linked with services like ORCID and GoogleScholar.


## Getting started, use a template 10
https://github.com/betatim/shablona walk through. You should recognise most
of this.

## binder 10
???How to make your repo run in the cloud???


# 6.30p The end
