Ksenia Prybylskaya,
Bioinformatics student, 2 year
Jagiellonian University
23.11.2026

This Homework Assignment 5 for BT4BR class.
# My Git Cheat Sheet

AI statement: I used AI for citing purposes.

Git provides developers and researchers with a dynamic and collaborative environment, often referred to as a social coding platform, that supports peer review, commenting, and discussion ((Dabbish et al., 2012, as cited in Perez-Riverol et al., 2016)

## Definitions

- SSH (Secure Shell) protocol - a protocol that lets communicate securily over unsecure networks (for example, a channel between a local repository and a remote one) (ylla-lab, 2026)
- Snapshot - every change to the tracked files, once committed, recorded as a new revision, uniquely identifying the changes in all the modified files. (Perez-Riverol et al., 2016)
- Commit - a single point in the Git history; the entire history of a project is represented as a set of interrelated commits. (Git Project, n.d.)
- Branch - a line of development (Git Project, n.d.)
- Master - the default development branch. (Git Project, n.d.)
- Merge - to bring the contents of another branch into the current branch. (Git Project, n.d.)
- Pull - pulling a branch means to fetch it and merge it. (Git Project, n.d.)
- Push - pushing a branch means to get the branch’s head ref from a remote repository, find out if it is an ancestor to the branch’s local head ref, and in that case, putting all objects, which are reachable from the local head ref, and which are missing from the remote repository, into the remote object database, and updating the remote head ref. If the remote head is not an ancestor to the local head, the push fails. (Git Project, n.d.)
- Head - a named reference to the commit at the tip of a branch. (Git Project, n.d.)
- Head ref - a synonym to head. (Git Project, n.d.)

## The Workflow
Working Directory -- `git add` --> Staging Area -- `git commit` --> Local Repository / Working Directory -- `git push` -- > Remote Repository

Remote Repository -- `git pull` --> Local Repository / Working Directory -- edit files --> `git add` --> Staging Area -- `git commit` --> Local Repository -- `git push` --> Remote Repository

## Commands (Step by Step by Perez-Riverol et al., 2016 and ylla-lab, 2026)

### 1. Move into directory to be tracked

`cd project`

### 2. Initialize local repository or Clone the existing one and then set up a local copy connected to the original remote repository.

`git init` or `git clone <URL>`

### 3. Add individual files such as project description, reports, source code

`git add README project.md code.R` stages these files' changes (selects the changes you want included in your next commit), including new untracked files. Use `git add -u` to stage changes to files Git already tracks.

### 4. Save the current local snapshot

`git commit -m "initial commit"` or `git commit`, if you don't include the message in a commit

### 5. Save the changes in GitHub

`git push origin main`

#### Also

Use `git status` to display the current state of your Git working directory and staging area to see which changes have been staged or not, and which files aren't being tracked by Git. Use `git diff` to see differences with last committed version.

## Work with branches 
`git branch <branch_name>` creates a branch.

Use `git checkout <branch_name>` and `git switch <branch_name>` for switching branches. Though, `git switch` is a newer one. `git checkout` has the functions of `git switch` and `git restore` together. For example, `git checkout <commit ID>` restores the changes that had been made by the time when this commit was made.

`git diff branch1..branch2` compares branches.

`git merge new_branch` brings the contents of `new_branch` to the current branch.

## If you have merging conflicts do

`git log --merge` to see the details, then edit the contents of the file where the conflict appeared, so that it works normally. Repeat the "Commands" section.

## Other basic commands
Use `git pull` to download from a remote repository and merge it with the local repository;

Use `git fetch` to download files from remote, but not merge with local;

Use `git show` to show the contents of a single commit.

## Resources

1.  Perez-Riverol Y, Gatto L, Wang R, Sachsenberg T, Uszkoreit J, Leprevost FdV, et al. (2016) Ten Simple Rules for Taking Advantage of Git and GitHub. PLoS Comput Biol 12(7): e1004947. <https://doi.org/10.1371/journal.pcbi.1004947>
2.  Git Project. (n.d.). Git glossary. Retrieved November 22, 2026, from <https://git-scm.com/docs/gitglossary>
3.  ylla-lab. (2026). BT4BR course 2026, Jagiellonian University [GitHub repository]. GitHub. [https://github.com/ylla-lab/BT4BR\\\_2026](https://github.com/ylla-lab/BT4BR_2026){.uri}
