#Chapter 2 : Git Basics

//Juntilla Gelsy

*Getting a Git Repository

  Initializing a Repository in an Existing Directory
    1. git init
    2. git add *.c
    3. git add LICENSE
    4. git commit -m "initial project version"
  Cloning an Existing Repository
    1. git clone url
    
*Recording Changes to the Repository

  Checking the status of Your Files
    1. git status
  Tracking New Files
    1. git add README
    2. git status
  Staging Modified Files
    1. git status
    2. git add CONTRIBUTING.md
    3. git status
    4. vim CONTRIBUTING.md
    5. git status
  Short Status
    1. git status -s
  Ignoring Files
    1. filename .gitignore
