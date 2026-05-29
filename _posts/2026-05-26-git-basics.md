---
layout: post
title: git basics
date: 2026-05-26 17:56 -0700
author: jlapsley
categories: [Notes]
tags: git
description: an intro to git, cli quick-reference guide
image:
    path: "assets/img/git-logo.png"
    alt: "sketch of git logo"
---
Git is a version control system. Used to store, track and manage code and files

I made this guide while studying for reference as I implement git into my workflow. 

#### Intro
- `git init` initializes the current directory, converting to a git repo
	- `git init <repo-name>` creates a new git repo with a name
- `git add` adds files/changes to the staging area
	- `. OR --all` adds all files to the staging area
- `git commit` saves (or commits) a file to the repo
	- `-m` adds a commit message 
- `git status` shows status of the staging and working area
####  Version History
- `git log` view git history
- `git diff` shows differences between commits
- `git revert` reverts entire repo to a previous commit
	- `-n` no commit occurs when reverting
	- `--no-edit` no commit message added
- `git checkout` reverts a single file 
- `git restore`  remove file from staging area
	- `git restore --staged <filename>`

#### Branches
- `git branch` lists the current branches
	- `*<filename>`  identifies the current branch
- `git branch <name>` creates a new branch
	- `-m <current-name> <new-name>` renames a branch
	- `-d <name>` deletes a branch  
	- `-D <name>` forcibly deletes a branch
	- **delete branches when they are no longer in use.** 
- `git switch <branch-name>` switches to a branch
	- `-c` creates, then switches to the newly created branch
- `git diff` shows differences between branches 
- ##### Merging
	`<source-branch>` - the branch being merged
	`<destination-branch>` the branch being merged into (usually main/master)
	switch to the `<destination-branch>`, then run the merge
- `git merge <source>` 
- *avoid editing the same files in multiple branches*
#### Remote
	remote repos are stored on a remote server, allows for collaboration between teams
- `git remote add <remote-name>` adds a name for a remote repo
- `git remote -v` lists all remotes
- `git clone` clones a  repo
- `get fetch origin` fetch all remotes from 
- `git merge` merges from remote
	- `git pull` fetches and merges
- `git push`push local to remote
#### Credentials
`git credential-cache exit` clears current git creds and prompts for new info



Feel free to leave a comment and share any commands you think I should add!
