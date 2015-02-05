# Chapter 5 : Distributed Git

//Gelsy Juntilla

* Distributed Workflows
  In Git, every developer is potentially both a node and a hub – that is, every developer can both contribute code to other repositories and maintain a public repository on which others can base their work and which they can contribute to.
  
  Centralized Workflow - One central hub, or repository, can accept code, and every one synchronizes their work to it.
  
  Intergation-Manager Workflow - Have a workflow where each developer has write access to their own public repository and read access to everyone else’s.
    1. The project maintainer pushes to their public repository.
    2. A contributor clones that repository and makes changes.
    3. The contributor pushes to their own public copy.
    4. The contributor sends the maintainer an e-mail asking them to pull changes.
    5. The maintainer adds the contributor’s repo as a remote and merges locally.
    6. The maintainer pushes merged changes to the main repository.
  
  Dictator and Lieutenants Workflow - It’s generally used by huge projects with hundreds of collaborators. Various integration managers are in charge of certain parts of the repository; they’re called lieutenants. All the lieutenants have one integration manager known as the benevolent dictator. The benevolent dictator’s repository serves as the reference repository from which all the collaborators need to pull. 
    1. Regular developers work on their topic branch and rebase their work on top of master. The master branch is that of the dictator.
    2. Lieutenants merge the developers’ topic branches into their master branch.
    3. The dictator merges the lieutenants’ master branches into the dictator’s master branch.
    4. The dictator pushes their master to the reference repository so the other developers can rebase on it.

* Contributing to a Project

  Variables:
      1. Active Contributor Count 
      2. Chosen Workflow
      3. Your Commit Access'
      4. External Contribution Method
      
