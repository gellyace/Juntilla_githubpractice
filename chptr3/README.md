#Chapter 3 : Git Branching

//Juntilla Gelsy

Branching - Diverge from the main line of development and continue to do work without messing with that main line. 

* Branches in Nutshell
  A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master. As you start making commits, you’re given a master branch that points to the last commit you made. Every time you commit, it moves forward automatically.
  A branch in Git is in actuality a simple file that contains the 40 character SHA-1 checksum of the commit it points to, branches are cheap to create and destroy. Creating a new branch is as quick and simple as writing 41 bytes to a file (40 characters and a newline).
  
  Creating a New Branch: git branch nameofbranch
  Switching Branches: git checkout nameofbranch
  
