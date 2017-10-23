# Git (notes from git-scm.com)

* version control system
* utilizes 'snapshots'
* doesn't store files that haven't changed from previous commit
* almost everything is local
* everything checksummed with SHA-1 hash
* almost only *adds* data, hard to lose changes
* **3 sections of a Git project:**
  * working directory: a single checkout of one version of the project; pulled out of the compressed database in the Git directory
  * staging area (a.k.a. 'index'): stores information about what will go into your next commit
  * .git directory (repo): where Git stores the metadata and object database for the project; this is copies when you clone a repo
* 
