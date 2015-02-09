#Chapter 2 : Git Basics

*Getting a Git Repository

  >Initializing a Repository in an Existing Directory
    Go to the project's directory and type: git init. This creates a new subdirectory named .git that contains all of your necessary repository files.
  >Cloning an Existing Repository
    To clone an existing repository, type: git clone [url]
    
	
*Recording Changes to the Repository

  >Two states in a working directory:
    ~Tracked files - files that were in the last snapshot and can be unmodified, modified, or staged
    ~Untracked files - files that were NOT in the last snapshot
  >Checking the status of Your Files
    To determine which files are in which state, type: git status.
  >Tracking New Files
    To begin tracking a new file, type: git add
  >Staging Modified Files
    Still use the git add command.
  >Short Status
    To have a more compact way of knowing the status, type: git status -s OR git status --short
	~?? - Files that aren't tracked
	~A - Files that have been added to the staging area
	~M - Modified Files
  >Ignoring Files
    To ignore files, create a .gitignore file and put the files you wanted Git to ignore there.
	  ~Rules for the patterns in.gitignore file:
	    1. Blank line or lines starting with # are ignored
	    2. Standard glob patterns work
	    3. You can end patterns with a forward slash(/) to specify a directory
	    4. You can negate a pattern by starting it with an exclamation point(!)
	  ~Special Characters:
	    1. Asterisk (*) - matches zero or more characters.
	    2. [_chracaters_] - matches any character inside the brackets
	    3. Question Mark (?) - matches a single character
	    4. ([_characters-characters_)] - matches any character between them
	    5. Two Asterisks (**) - match nested directories
  >Viewing Your Staged and Unstaged Changes
    To know exactly what you changed (unstaged), type: git diff
	To see what you've staged that will go into your next commit, type: git diff --staged
	To see what you've staged so far, type: git diff --cached
  >Committing Your Changes
    To commit, type: git commit
  >Skipping the Staging Area
    To skip the staging area (or the git add part), add the -a option to the git commit command.
  >Removing Files
    To remove file from the local directory, type: rm filename
    To remove file from your tracked files, type: git rm filename
    To keep the file in your working tree but remove it from your staging area, type: git rm --cached README
    To remove all files that have .[extension] in the [folder]/ dirctory, type: git rm [folder]/\*.[extension]
    To remove all files that end with [character], type: git rm \*[character]
  >Moving Files
    To rename a fil in Git, type: git mv [file_from] [file_to]

	
* Viewing the Commit History
  >To look back what has happened in your commits, type: git log
  >To view the difference between each commit, type: git log -p
  >To limit the result to the only last two entries, type: git log -2
  >To view the abbreviated stats for each commit, type: git log --stat
  >To limit the Log Output, type: gi log --since=dateyouwanted
  
  
* Undoing Things
  >To try a certain commit again, type: git commit --amend
  >To unstage a staged file, type: git reset HEAD [file]
  >To unmodify a modified file, type: git checkout -- [file]
  
  
* Working with Remotes
  >Remote Repositories - versions of your project that are hosted on the Internet or network somewhere.
  >To show which remote servers you have configured, type: git remote
  >To add Remote Repositories, type: git remote add [shortname] [url]
  >To get data from your remote projects, type: git fetch [remote-name]
  >To push a project into the upstream, type: git push [remote-name] [branch-name]
  >To see more information about a particular remote, type: git remote show [remote-name]
  >To rename a remote, type: git remote rename [oldname] [newname]
  >To remove a remote, type: git remote rm [name]
  
  
* Tagging
  >To list the tags available, type: git tag
  >Creating Tags:
    ~Lightweight Tag - very much like a branch that doesn't change - it's just a pointer to a specific commit.
	  git tag [name]
    ~Annotated Tag - stored as a full object in the Git database, and are checksummed.
	  git tag -a [name] -m [tagging message]
  >To push tags to a shared server, type: git push origin [tagname]
  >To put a version of your repository in your working directory that looks like sa specific tag, type: git checkout -b [newbranch] [tag]
  
  
* Git Aliases
  >To create an alias, type: git config --global alias.[name] 'equivalent command'
  
	
	
