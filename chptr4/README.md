# Chapter 4 : Git on the Server


* The Protocols
  >Local Protocol -  the remote repository is in another directory on disk. Often used if everyone on your team has access to a shared filesystem such as an NFS mount, or in the less likely case that everyone logs in to the same computer.
    ~The Pros:
      1. Simple
      2. They use Existing File permissions and network access.
      3. Nice option for quickly grabbing work from someone else's working repository
    ~The Cons:
      1. Shared Access is generally more difficult to set up and reach from multiple locations than basic network access.
      2. Isn't the necessarily fastest option if you're using a shared mount of some kind
      
  >The HTTP Protocols - it’s simpler for the user and smarter about how it communicates.
    Dumb HTTP - expects the bare Git repository to be served like normal files from the web server.
    Smart HTTP - operates very similarly to the SSH or Git protocols but runs over standard HTTP/S ports and can use various HTTP authentication mechanisms
      ~The Pros:
        1. Simplicity of having a single URL for all types of access
        2. Being able to authenticate with a username and password
        3. Commonly used protocols that corporate firewalls are often set up to allow traffic through these ports.
      ~The Cons:
        1. More tricky to set up compared to SSH on some servers
        2. Very little advantage that other protocols have over the “Smart” HTTP protocol for serving Git.
        
  >The SSH Protocol - A common transport protocol for Git when self-hosting. 
      ~The Pros:
        1. Easy to set up
        2. Access over SSH is secure
        3. Efficient
      ~The Cons:
        1. You can’t serve anonymous access of your repository over it.
        
  >The Git Protocol - It listens on a dedicated port (9418) that provides a service similar to the SSH protocol, but with absolutely no authentication
      ~The Pros:
        1. Often the fastest network transfer protocol available
      ~The Cons:
        1. Lack of authentication

* Getting Git on a Server
  >To clone your repository to create a new bare repository, type: git clone --bare [repo] [bare repo]

* Generating Your SSH Public Key
  1. cd ~/.ssh
  2. ls
  3. cat ~/.ssh/id_rsa.pub
  
* Setting Up the Server
  
* Git Daemon

* Smart HTTP

* GitWeb

* GitLab
