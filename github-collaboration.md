# Collaborating on GitHub

Collaborating with others to work on the same repository can be quite confusing.
The fact that there are many different ways that you could work together does
not help. This tutorial describes one way. It is what most open-source
projects seem to have settled on. It finds the right balance between learning
curve and usefulness.

This tutorial starts with the assumption that there is a project to which you
would like to contribute. This project already exists as a repository on GitHub.
You will make a copy of the repository, make changes and then ask for these
changes to be integrated into the original repository.

We will use https://github.com/YOURPARTNERSNAME/zuri-velo to practice. In
the language of GitHub "making a copy" is referred to as "forking". Requesting
that your changes are integrated into the original repository goes by the name
of "making a pull request".


## Creating a Fork

Head over to the GitHub page of https://github.com/YOURPARTNERSNAME/zuri-velo.
To fork it click the "Fork" button. Once you've done that, you can use your favorite git
client to clone your copy of the repository:

```
# Clone your fork to your local machine
git clone https://github.com/YOURNAME/zuri-velo
```

## Making your changes

Whenever you begin work on a new topic it's important that you create a new
branch. This keeps your changes organised and separated from the master branch
so that you can easily submit and manage multiple pull requests for every task
you complete.

To create a new branch and start working on it:

```
# Checkout the master branch - just to make sure
git checkout master

# Create and switch to your new branch
git checkout -b adding_contributors
```

Now you can make your changes, in this case adding a section mentioning who has
contributed to this repository. Then add and commit your changes as we did before:
```
# change the README to add contributors, then
git add README.md
git commit -m "Add section on contributors"
git push
```

If you now visit https://github.com/YOURPARTNERSNAME/zuri-velo the web interface will
suggest to you that you can create a pull request. The GitHub documentation is
pretty good: https://help.github.com/articles/about-pull-requests/

Congratulations, you have made your first pull request!


# Exercise

Fork the `zuri-velo` repository, clone it to your laptop, create a new branch,
edit the README, add a section naming the collcommit your changes, push your
changes to GitHub and create a pull request.

---

## Accepting a pull request

To complete the next step, switch roles into being the owner of the original
repository http://github.com/USER_A/zuri_velo. You should see a new pull request,
it shows you the changes that were proposed and any messages from the person
who created the pull request. After reviewing things, and maybe asking some
follow up questions, you can click the big green button at the bottom of the
page to accept the changes.

https://help.github.com/articles/reviewing-changes-in-pull-requests/


## Going further

This is just a short tutorial, you can find more details and explanations in
the GitHub documentation:

* [Working with forks](https://help.github.com/articles/working-with-forks/)
* [Proposing changes](https://help.github.com/articles/proposing-changes-to-your-work-with-pull-requests/)
