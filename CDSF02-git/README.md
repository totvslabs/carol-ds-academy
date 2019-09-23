# Git and GitHub

## What is GIT?

Git? Is that another name for GitHub?

Nope.

Git is a software that helps you keep track of changes to files in a folder on your PC.

These changes could be creating, renaming, deleting a file or subfolder; or editing the content of a file.

After making some changes to files in this folder, you can “commit” the changes to Git for safe-keeping.

## Installing Git

Debian/Ubuntu Linux:

`$ sudo apt-get install git-all`

RedHat/Fedora Linux:

`$ sudo yum install git-all`

MacOS:


Install Xcode Command Line Tools or download from https://git-scm.com

Windows:


Download from https://git-scm.com or use Chocolatey to install:

`C:\> choco install git`

## Git Basics

### Identify yourself

Git needs to know who you are to track all changes on git manager files.

`git config --global user.name “Your Name Comes Here”`
`git config --global user.email you@yourdomain.example.com`

### Initializing a local repository

We have to prepare a folder to be managed by git.

In an empty folder:

`git init`

You can also use git to create a folder with a local repository

`git init <folder>`

[]("images/render1568762028353.gif")

### Understanding Git philosophy

#### History

A.K.A. Local repository, everything git is stored here (.git folder)

#### Stage (Index)

Files you want to commit. Before you “commit” (checkin) files, you need to first add them to the index. Also called "current directory cache", "staging area", "cache" or "staged files".

#### Working Directory

The folder you are working.

### Files operation in a git repository

Add New/Modified file to Stage

`git add <files | *>`

Commit Stage to Repository

`git commit [-m <Message>] [-a]`

Check current repository status

`git status [-s]`

Remove file from repository

`git rm [--cached] <file>`

[]("images/render1568763039432.gif")

### Repository operation in a git repository

Unstage a file (before commit) but keeping it modified

`git reset -- <file>`

Restore a unstaged file from previous commit

`git checkout -- <files>`

Checkout Stage to Repository

`git checkout <commit id|branch|tag>`

[]("images/render1568776290681.gif")

### Tags (A.K.A. Versions)

Recording a new Tag to the current commit

`git tag <tag id> [<commit_id>]`

List current repository tags

`git tag [-l "<pattern>"]`

Checkout a tag

`git checkout <tag>`

## Working with others

Everything until now is only available to you. It's time to share your code. Now, we gonna work with Git Remote repositories. A remote repository is generally a bare repository. In the simplest terms, a bare repository is the contents of your project’s .git directory and nothing else.

### Git Remote Repositories operations

Clone a repository to a local repo

`git clone <repo url>`

Retrieve all data from remote without merge

`git fetch`

Retrieve all data from remote and merge

`git pull`

Push your commits to remote

`git push [<remote>] [<branch>]`

### GitHub

GitHub is the most famous remote git cloud provider. They provides to the community

- Remote Git repositories (duh!)
- Code Review Tools
- Project Management Tools
- Task/Issue Manager
- Agile Management Tools
- Oauth2 Authentication Provider
- Lot of integrationsCI/CD platform
- and more...

### Github Remote Repository Workflow

![img](https://lh5.googleusercontent.com/bVpYXTGfJKvd7vbTto6rWXhzi3SdC25FpO96eCw3OSS-8A70C54WJLgORw0EsdA0ccDoe4DEf-jiyQtE9brXTLyAyR6yQLet_C53_T4BRvWzSuxUzchsXKRAzdiEwMULNEDKjYrf25c)

#### Create a branch

When you're working on a project, you're going to have a bunch of different features or ideas in progress at any given time – some of which are ready to go, and others which are not. Branching exists to help you manage this workflow.

When you create a branch in your project, you're creating an environment where you can try out new ideas. Changes you make on a branch don't affect the master branch, so you're free to experiment and commit changes, safe in the knowledge that your branch won't be merged until it's ready to be reviewed by someone you're collaborating with.

#### Add commits

Once your branch has been created, it's time to start making changes. Whenever you add, edit, or delete a file, you're making a commit, and adding them to your branch. This process of adding commits keeps track of your progress as you work on a feature branch.

Commits also create a transparent history of your work that others can follow to understand what you've done and why. Each commit has an associated commit message, which is a description explaining why a particular change was made. Furthermore, each commit is considered a separate unit of change. This lets you roll back changes if a bug is found, or if you decide to head in a different direction.

#### Open a Pull Request

Pull Requests initiate discussion about your commits. Because they're tightly integrated with the underlying Git repository, anyone can see exactly what changes would be merged if they accept your request.

You can open a Pull Request at any point during the development process: when you have little or no code but want to share some screenshots or general ideas, when you're stuck and need help or advice, or when you're ready for someone to review your work. By using GitHub's @mention system in your Pull Request message, you can ask for feedback from specific people or teams, whether they're down the hall or ten time zones away.

#### Discuss and review your code

Once a Pull Request has been opened, the person or team reviewing your changes may have questions or comments. Perhaps the coding style doesn't match project guidelines, the change is missing unit tests, or maybe everything looks great and props are in order. Pull Requests are designed to encourage and capture this type of conversation.

You can also continue to push to your branch in light of discussion and feedback about your commits. If someone comments that you forgot to do something or if there is a bug in the code, you can fix it in your branch and push up the change. GitHub will show your new commits and any additional feedback you may receive in the unified Pull Request view.

#### Deploy

With GitHub, you can deploy from a branch for final testing in production before merging to master.

Once your pull request has been reviewed and the branch passes your tests, you can deploy your changes to verify them in production. If your branch causes issues, you can roll it back by deploying the existing master into production.

#### Merge

Now that your changes have been verified in production, it is time to merge your code into the master branch.

Once merged, Pull Requests preserve a record of the historical changes to your code. Because they're searchable, they let anyone go back in time to understand why and how a decision was made.

### Github Workflow - Best Practices

- Avoid push directly do master branch
- Do git commit with the right email address
- Always use pull requests and ask for code reviews
- Create a meaningful git ignore file (https://www.gitignore.io/)
- Don't commit without a good commit message (see https://www.conventionalcommits.org/)
- Be nice, review code, ask for code review

## Read More

- Git Pro eBook - https://git-scm.com/book/en/v2
- Visual Git Reference - http://marklodato.github.io/visual-git-guide/index-en.html
- Visualizing Git Concepts with D3 - http://onlywei.github.io/explain-git-with-d3/
- Git Visual CheatSheet - http://ndpsoftware.com/git-cheatsheet.html
- GitHub Documentation - https://help.github.com/en#dotcom

