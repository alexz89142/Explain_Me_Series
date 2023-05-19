## NOTE: ⚠️ Still under construction ⚠️

# How does storage in Proxmox VE work?
If you're currently learning Proxmox and haven't used NAS or server technology much before, you might find youself following a guide and asking yourself this simple question. I want to take a second to step back and show the overview of ProxMox storage.

The purpose of this article is to give an explanation for the concepts listed

## Storage Options
For the most part there are three ways to use storage in Proxmox:
- Passing a drive directly through to a virtual machine
- Creating a pool (a collection of drives) and writing data to it in Proxmox
- Shared storage

Each of these has their own complexities and benefits

### Passing a drive in
Passing a drive directly into the virtual machine has a pretty simple trade off
Pros:
- It's useage is simple. The VM treats it as an actual physical disk and data is written to it normally
- Performance
- Can be set up so that the disk can be accessed in a VM and also booted natively
Cons:
- The disk becomes inaccessible to any other VM

### Shared storage
Pros:
- Storage is accessible to multiple virtual machines
Cons:
- More complex setup

### Storage pool
A storage pool is most likely what you're going to be using if you have a single virtual machine application
Pros:
- Simple setup
- More versatile
Cons:
- Not as performant as passing the disk in

We're going to focus on storage pools

### Storage types
When you set up a storage pool it must be one of a couple different storage types. 
They are as follows:
- LVM
- LVM-Thin
- Directory
- ZFS

Each one has it's own benefits and limitations. More information is avaiable on the [Proxmox Wiki](https://pve.proxmox.com/wiki/Storage)

#### LVM
- Supports 

#### LVM-Thin

#### Directory

#### ZFS