# Get Down with git [![Build Status](https://travis-ci.org/sarahelizgray/get_down_with_git.svg?branch=master)](https://travis-ci.org/sarahelizgray/get_down_with_git)

![dance dance dance](http://i.giphy.com/l46C8nSNYWU567Hs4.gif)

# OVERVIEW
* what is source control and why is it important.
* Touch on other source control options and hosts.
* Source control is one aspect of professional deploy cycle -- works hand in hand with continuous integration and the code review process.
* It's more than just checking in code, it's leaving a breadcrumb trail for ourselves and our partners to understand how and why we constructed things the way we did. Great for your upcoming team project!

#REVIEW:
* review of basic git idiom
* Gives you lots of beak points. 'git reset' to previous working commit.
* companion to existing best practices around "test a little, write a little."
* Gets stuff off your machine!
* Build your portfolio for interviewing!

## Review of basic git idiom 
|Git Command       |Summary     |
|------------------|------------|
|git pull          |get most recent commits from the branch you are on|
|git add <filename>|this file or all changes in this file to staging|
|git commit -m     |combine all things in staging into a commit bundle with this message on my local machine|
|git push          |push all of my local commits up to the remote branch on the remote repo|
|git status        |see status of local repo, what's changed, what's committed, what's new|

##Some tips and tricks
|Git Command       |Summary     |
|------------------|------------|
|git add -p        |cycle though all tracked files and inspect changes one at a time|
|git diff          |show me, line by line, what has changed in tracked files that aren't added|
|git diff --cached |show me, line by line, what has changed in added files|
|git commit --ammend|alter the commit message of a staged commit|


# SEE HOW IT IMPROVES YOUR WORKFLOW
* check out the log, see that you've left yourself some notes
* revert back to some previous state easily

## Git Log
|Git Command       |Summary     |
|------------------|------------|
|git log           |show long form commit info|
|git log --pretty=oneline| show short form commit info|
|git reset --hard <some commit id>|turn back time on my local machine to some previous commit id|
|git reset --hard HEAD@{<number of commits back>}|turn back time on my local machine to some number of commits back|


#FOR YOUR TEAM/PROFESSIONALLY:
##Git Flow
##Fork and Pull
[http://blog.ieeesoftware.org/2015/12/variability-management-using-github.html](assets/fork_and_pull.png)

## Shared Repo
[http://hades.github.io/2010/01/git-your-friend-not-foe-vol-2-branches/](assets/git-history.png)

##Branch Management
###branch creation idiom
|Git Command       |Summary     |
|------------------|------------|
|git branch <some branch name>|create a branch on your local machine|
|git push -u origin <some branch name>|push your local branch to the remote|
|git branch|see all my local branches|
|git checkout <some branch name>|switch to a local branch|

###branch management commands
|Git Command       |Summary     |
|------------------|------------|
|git branch -a|see my local and remote branches|
|git checkout --track origin<some remote branch name>|get a remote branch on your local machine|
|git branch -d <some local branch name>|delete the local branch|
|git branch -D <some local branch name>|force delete the local branch|
|git push -u origin <some remote branch name>|delete a remote branch|

##Merging and Resolving Merge Conflicts
|git merge <some local branch name>|apply commits from some other the local branch to the current branch you are in|

##The Stash
|Git Command       |Summary     |
|------------------|------------|
|git stash|put any tracked changes into stash|
|git stash save "<some note about what is stashed>"|leave yourself a note about what you are stashing|
|git stash list|see a list of what is stashed|
|git stash pop|take the first item off the top of the stash|
|git stash clear|wipe out the stash|

##Rebasing
|Git Command       |Summary     |
|------------------|------------|
|git rebase <some local branch name>|alter history. replay all of my commits on top of current local version of some other branch. Must `git push -f` (force push to commit to remote) to apply this to the remote|

##Squashing
|Git Command       |Summary     |
|------------------|------------|
|git rebase -i <some local branch name or commit id>|alter history. combine commits, delete commits, reword commit messages. Must `git push -f` (force push to commit to remote) to apply this to the remote|

##The Reflog
|Git Command       |Summary     |
|------------------|------------|
|git reflog|see the history of branches across the whole repo



#FOR OPEN SOURCE CONTRIBUTIONS: 
Branches are used to manage not just feature creation but also the life cycle and continued development of many projects. 
Shout out to how open source projects like the development of Rust http://2016.phillyemergingtech.com/session/stability-without-stagnation-lessons-learned-shipping-ember/.
SUMMARY: It's a handy, essential tool that you can use today to improve your development experience. 

#Resources
* the scm

