#Chapter 6 : GitHub 



>GitHub - single largest host for Git repositories, and the central point of collaborations for millions of developers and projects. A large percentage of all Git repositories are hosted on GitHub but it isn't a direct part of the Git open source project.

* Account Setup and Configuration

>Set up a free user account : https://github.com
>Verify your account through the email you used.

>SSH Access - "Generating Your SSH Public Key"
  1. Open up your account settings in GitHub
  2. Select "SSH keys" section along the left-hand side.
  3. CLick the "Add an SSH key" button and paste the contents of your ~/.ssh/id_rsa.pub (or whatever you named it) and click   "Add key"
  
>Your Avatar - Profile Picture
 1. Go to the "Profile" tab (above the SSH Keys tab)
 2. Click "Upload new picture"

>Your Email Addresses - the way GitHub maps your Git commits to your user is by email address
 You can add multpile email addresses, all you need is to add all of these to the Emails section of the admin section of GitHub.
  ~Two Factor Authentication or "2FA" - an authentication mechanism to mitigate the risk of your account being compromised if your password is stolen somehow. This will ask two different methods of authentication.
    To Setup : Security Tab of the Account Settings -> click on the "Set up two factor authentication" button


* Contributing to a Project

>Forking Projects - GitHub will make a copy of the project that is entirely yours; it lives in your user's namespace, and you can push to it.
  To fork a project: Vist the project page and click the "Fork" button.
  
>The GitHub Flow
  1. Create a topic branch from master.
  2. Make some commits to improve the project.
  3. Push this branch to your GitHub project.
  4. Open a Pull Request on GitHub.
  5. Discuss, and optionally continue committing.
  6. The project owner merges or closes the Pull Request.

  ~Creating a Pull Request ( lets you tell others about changes you've pushed to a repository):
    1. Click the "Fork" button to get our own copy of the project
    2. Clone it locally in your machine
    3. Create a topic branch
    4. Make the Code change
    5. Check that the change is good
    6. Commit our change to the topic branch
    7. Push the changes back up to GitHub
    8. Click the "Compare and Pull Request" button
    OR
    Go to the "Branches" page : https://github.com/<user>/<project>/branches and open a new Pull Request form.
    
    The owner of the project may merge it, reject it, or comment on the suggested idea.
    
    ~Keeping up with the Upstream - Pull Request becomes out of date or doesn't merge cleanly.
      1. Add the original repository as a remote named "upstream"
      2. Fetch the newest work from that remote
      3. Merge the main branch into your topic branch
      4. Fix the conflict that occured
      5. Push back up to the same topic branch
      With this the Pull Request will automatically be updated and rechecked to see if it merges cleanly.
      
    ~References
      ~~Cross-reference another Pull Request or an Issue:
        Simply put #<num> in any comment or description
        OR
        Write username#<num> if you're refering to an Issue or Pull Request in a fork of the repository you're in
        OR
        Write username/repo#<num> to reference something in another repository
      ~~Reference a specific commit using SHA-1:
        Specifiy a full 40 chracater SHA-1
        OR Just do the same steps in Cross-referencing another Pull Request or an Issue.
        
    ~Markdown - like writing in plain text but which is rendered richly
      ~~Task List - specific Markdown feature, especially for use in Pull Requests. It is a list of checkboxes of things you want to get done.
        Example:
          - [X] Write the code
          - [ ] Write all the tests
          - [ ] Document the code
      ~~Code Snippets - useful if you want to present something that you could try to do before actually implementing it as a commit on your branch.
        To add a snippet of code you have to “fence” it in backticks.
          ```java
          for(int i=0 ; i < 5 ; i++)
          {
           System.out.println("i is : " + i);
          }
          ```
      ~~Quoting - If you’re responding to a small part of a long comment, you can selectively quote out of the other comment by preceding the lines with the > character.
      ~~Emoji - actually used quite extensively in comments you see on many GitHub Issues and Pull Requests.
      ~~Images - isn’t technically GitHub Flavored Markdown, but it is incredibly useful.
      
	  
* Maintaining a Project
>Creating a New Repository
  Start by clicking the "New Repository" button on the right-hand side of the dashboard, or from the + button in the top toolbar next to your username, and provide the necessary details.
>Adding Collaborators
  Click the "Settings" link at the bottom of the right-hand sidebar, then select "Collaborators" from the menu on the left-hand side. Then, just type a username into the inbox, and click "Add collaborator"
>Managing Pull Requests
>Special Files
  ~README - holds all the relevant project information
  ~CONTRIBUTING - specify the things you want or don't want in aPull Request sent to your project
  
  
* Managing an organization
>Organization Basics
  To create a new organization: Start by clicking the "New Organization" button on the right-hand side of the dashboard, or from the + button in the top toolbar next to your username, and provide the necessary details.
>Teams
>Audit Log


* Scripting GitHub

>Services and Hooks - gives you a way to receive push notifications about events that happen on your repositories
>The GitHub API
  ~Basic Usage
  ~Commenting on an Issue
  ~Changing the Status of a Pull Request
  
  
