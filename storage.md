# gcrNet Storage Environment

Network storage is part of the gcrNet core services provided. This includes storage available to all users with a gcrNet account and for gcrNet registered projects. Network storage can be accessed directly while on the gcrNet network. The Data Transfer Node (Globus) should be used to transfer data in and out of the gcrNet.
(This documentation if for user so, I will only mention Globus and not the DatTransfer Node)
- gcrNet
  - /home
  - /data/project
  - /data/scratch

## Home Directories

Home directories are provided to all gcrNet user accounts. This storage is provided by a RAID 5 storage group on GenLogin, with a total of 6.6TB available storage.
(Maybe leave out technical detail and focus the message, state what it is, where it is and how to get it)
The default user quota is 50GB hard/soft limits.

* Path: /home/<username>
* Size: 50 GB (I suggest 10GB, 50GB is approx. 132 accounts that could be maxed out for two institution. This will also be tempting to run jobs on the genlog)
* Home directory size could be increased if justified ?
* How to access (landing point after login)
* Is this backed up?  

## Project Storage

Each registered project on the gcrNet receives a project directory that is located on the Data Transfer Node, and accessible on the gcrNet via NFS. This storage is provided by a RAID 5 storage group on the DTN with a total of ~30TB available storage. 

* Path: /data/project
* Size: (Generally 1TB and could be increased if justifiable)  
* Is this to be backup?
* How to Access it (generally soft link in the user's home directory)?
* Softlink, allows for group setup and move data in/out without ssh into the DTN
* Project directory and group naming convention?
* At setup, Proj. directory should have one owner and a project group name (id)
* Process to add member to project group (explicite permission from PI?)

  
## Scratch Storage
Scratch space is available to all gcrNet users and is located on the Data Transfer Node. This space is comprised of ~5TB high speed solid state drives for temporary usage.
  
* Path: /data/scratch
* Only available on compute nodes? (This what scratch is for)
* Naming convention for directories (have this in job's script)
* Acess. Scratch is accessible on the compute node. Therefore, only users with access to compute node can access scratch
* How long after job completion before the directory is deleted?
* Should the admin request PI to cleanup or should admin clean up? 
* What is the threshold for purging (90%?) 
* What is the priority order for purging?

## Accessing Storage
  
Globus availability and accessibility should be discussed here. We should make sure information about a partition in under the section for that partition
* I suggest, /data/project/ for root of mapped collection
* Guest collection used to give PI globus access to their project directory.
* Make PIs administrators of their guest collection
* Creat softlink to project directory in PI's and project member's home dir.
* PI will managed data sharing through globus (setting permisions and assigning specific directories)
  


gcrNet storage can be accessed in two ways: directly on the gcrNet and through Globus. Direct access is available when connected to the gcrNet allowing the user to store data from insturmentation or compute environments located on the network. Globus access provides a way for users to access, share, and transfer data outside of the gcrNet.

** Note - Globus and direct permissions do not match. **

### Globus Access

Home directories are made available in Globus using a Guest Collection that is shared with the users home institution username.

Each project directory is shared with the PI using the PIs home institution username. The PI can then share with additional project members.

### Direct Access

Storage is accessed directly on the gcrNet by connecting to genlogin using your gcrNet account using the paths described above.

## Special Storage Requests

The gcrNet can accomodate additional storage options for projects that require the user of specialized storage. Please contact the gcrNet technical team prior to purchasing storage solutions to ensure compatability with the network.
