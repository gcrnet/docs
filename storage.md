# gcrNet Storage Environment

Network storage is part of the gcrNet core services provided. This includes storage available to all users with a gcrNet account and for gcrNet registered projects. Network storage can be accessed directly while on the gcrNet network. The Data Transfer Node (Globus) should be used to transfer data in and out of the gcrNet.

- gcrNet
  - /home
  - /project
  - /scratch

## Home Directories

Home directories are provided to all gcrNet user accounts. This storage is provided by a RAID 5 storage group on GenLogin, with a total of xTB storage available.

## Project Storage

Each registered project on the gcrNet receives a project directory that is located on the Data Transfer Node, and accessible on the gcrNet via NFS.

## Scratch Storage

Scratch space is available to all gcrNet users and is located on the Data Transfer Node. This space is comprised of high speed solid state drives for temporary usage.
