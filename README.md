#http fs
WIP

The idea is to have a virtual file that allows reading from a file retrieved via http. Currently the url for the file is taken from the clipboard, and if the connection fails (e.g. because the URL is invalid) the file cannot be opened.

This is ment to be useful when having a screenshot tool that uploads images/videos/text etc. to a server but you want to e.g. tweet an image, so you dont have to manually download and later manually delete the file.

The project is written in [PointerScript](https://github.com/M4GNV5/PointerScript) using [libfuse](https://github.com/libfuse/libfuse) for creating a virtual userspace filesystem.

You can mount the fs using `ptrs src/main.ptrs MOUNTPOINT` and unmount it using `fusermount -u MOUNTPOINT`
