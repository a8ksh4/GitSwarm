# GitSwarm
Inspired by GitHub - Distributed development platform that is Secure, Social, and Resiliant

Input requested :)

Components:
* Client Software - cmnd line -> gui
* Key Management - 
* Tracker Integration
* Distributed user identity - user only needs private key. 

Projects that use similar tech:
* Gittorrent - http://code.google.com/p/gittorrent/
* Delugefs - http://code.google.com/p/delugefs/ They have some interesting research posted up here. 
* Freenet, Bitcoin, There have been some sneakernet proposals for 3rd world that might be interestign. 

Notes... Local repo is just like normal, but repo initialization, clone, push, pull, etc. all depend on custom clinet.

Design Musings:
* No user/acct management... users sign their code.  Branches/changes are merged by signing code.  Have to work out logistics of how this happens as I learn more about git protocols and bitorrent. 
* Repo create includes public key for the repo.  Pushes are incremental and signed to ensure validity.  
* Client includes default trackers to publish to.  
* Levarage t
* I'm curious how something like this could work in tandem 
* How does the client emulate the git server?  It could serialize writes to a VFS (that appears like a local/nfs git server repo) and packege them into torrent packages.  This threats bittorrent like a virtual file system storage... does that simplify the prob?
* How to manage locks and race conditoins when making commits?  Bitcoin sues network majorirty to enablelocking or commit priority.  What if we make it appear that every owner has the main branch, and all other commits are merge requests?  They can subscribe to another main branch.

