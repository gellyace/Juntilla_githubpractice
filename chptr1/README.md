#Chapter 1 Summary



* About Version Control

>Version Control - A system that records changes to a file or set of files over time so that you can recall specific versions later

>Version Control System - Allows you to revert files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modifies omething that might be causing a problem, who introduced an issue and when. 

~Local Version Control Systems - a simple database that kept all the changes to files under revision control in your directory. A popular VCS tool is the RCS system which works by keeping patch sets (that is, the differences between files) in a special format on disk; it can then re-create what any file looked like at any point in time by adding up alll the patches.

~Centralized Version Control Systems - have a sinle server that contains all the versioned files, and a number of clients that check out files from that central place. This had been the standard for version control.

~Distributed Version Control Systems - clients don't just check out the latest snapshot of the files: they fully mirror the repository. If any server dies any of the client repositories can be copied back up to the server to restore it. Every clone is really a full backup of all the data.


* A Short History of Git

>Linux Kernel - open source software project of fairly large scope. 
>2002 - Linux Kernel Project began using a proprietary DVCS called BitKeeper.
>2005 - relationship between the Linux kernel developers and the BitKeeper developers broke down, and the tool's free-of-charge status was revoked. 
>Linus Torvalds, the creator of Linux, developed their own tool based on some of the lessons they learned while using BitKeeper which was now the popular Git.


* Git Basics

>Git thinks of its data as a set of snapshot of a miniature filesystem or more likely a stream of snapshots.
>Most operations of Git only need local files and resources to operate.
>Everything in Git is check-summed before it is stored and is then referred to by that checksum, so Git will always know if there is any changes being made. 
~SHA-1 hash - mechanism used by Git for checksumming. It is a 40-charactr string composed of hexadecimal characters (0-9 and a-f) and calculated based on the contents of a file or directory structure in Git.
>Git generally only add data to the Git database.
>Three main states that your files can reside in :
~Commited - data is safely stored in your local database
~Modified - you have changed the file but have not commited to your database yet
~Staged - you have marked a modified file in its current version to go into your next commit snapshot.
>Three main sections of a Git project:
~Git Directory - where Git stores the metadata and object database for yor project. Most important part of Git.
~Working Directory - single checkout of one version of the project
~Staging Area - a file, generally in the Git directory, that stores information about what will got into your next commit. It is referred to as the "index".
>The basic Git workflow:
1. You modify files in your working directory
2. You stage the files, adding snapshots of them to your staging area
3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git Directory

* The Command Line

>The command line is the only place you can run all the Git commands.
>Installing Git (please refer to chapter1_answers)
>Setting up GitHub (also please refer to chapter1_answers)




