# gcrNet Storage Environment

Network storage is part of the gcrNet core services provided. This includes storage available to all users with a gcrNet account and for gcrNet registered projects. Network storage can be accessed directly while on the gcrNet network. The Data Transfer Node (Globus) should be used to transfer data in and out of the gcrNet.

- gcrNet
  - /home
  - /data/project
  - /data/scratch

## Home Directories

Home directories are provided to all gcrNet user accounts. This storage is provided by a RAID 5 storage group on GenLogin, with a total of 6.6TB available storage.

The default user quota is 50GB hard/soft limits.

/home/<username>

## Project Storage

Each registered project on the gcrNet receives a project directory that is located on the Data Transfer Node, and accessible on the gcrNet via NFS. This storage is provided by a RAID 5 storage group on the DTN with a total of ~30TB available storage.

/data/project

## Scratch Storage

Scratch space is available to all gcrNet users and is located on the Data Transfer Node. This space is comprised of ~5TB high speed solid state drives for temporary usage.
  
/data/scratch

## Accessing Storage

gcrNet storage can be accessed in two ways: directly on the gcrNet and through Globus. Direct access is available when connected to the gcrNet allowing the user to store data from insturmentation or compute environments located on the network. Globus access provides a way for users to access, share, and transfer data outside of the gcrNet.

### Globus Access

Home directories are made available in Globus using the mapped collection named 'gcrNet DTN - Users'. 

Each project directory is available using the mapped collection 'gcrNet DTN - Projects'. The PI can then share with additional project members.

### Direct Access

Storage is accessed directly on the gcrNet by connecting to genlogin using your gcrNet account using the paths described above.

## Special Storage Requests

The gcrNet can accomodate additional storage options for projects that require the user of specialized storage. Please contact the gcrNet technical team prior to purchasing storage solutions to ensure compatability with the network.
