#Chapter 3 : Git Branching


Branching - Diverge from the main line of development and continue to do work without messing with that main line. 

* Branches in Nutshell

  A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master. As you start making commits, you’re given a master branch that points to the last commit you made. Every time you commit, it moves forward automatically.
  A branch in Git is in actuality a simple file that contains the 40 character SHA-1 checksum of the commit it points to, branches are cheap to create and destroy. Creating a new branch is as quick and simple as writing 41 bytes to a file (40 characters and a newline).
  
  Creating a New Branch: git branch nameofbranch
  Switching Branches: git checkout nameofbranch
  

* Basic Branching and Merging

  Let’s go through a simple example of branching and merging with a workflow that you might use in the real world. You’ll follow these steps:
    1. Do work on a web site.
    2. Create a branch for a new story you’re working on.
    3. Do some work in that branch.
  At this stage, you’ll receive a call that another issue is critical and you need a hotfix. You’ll do the following:  
    1. Switch to your production branch.
    2. Create a branch to add the hotfix.
    3. After it’s tested, merge the hotfix branch, and push to production.
    4. Switch back to your original story and continue working.


* Branch Management
  >git branch


* Branching Workflows

  ~Long-Running Branches - you can have several branches that are always open and that you use for different stages of your development cycle
  ~Topic Branches - short-lived branch that you create and use for a single particular feature or related work. 


* Remote Branches -  references (pointers) to the state of branches in your remote repositories. These act as bookmarks to remind you where the branches on your remote repositories were the last time you connected to them


* Rebasing - take all the changes that were committed on one branch and replay them on another one.
  >Do not rebase commits that exist outside your repository
  
  
