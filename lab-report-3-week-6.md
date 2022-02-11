# CSE 15L Lab Report 3: Copy Directories with `scp -r`
When it comes to directories, `scp` has some limitations. `scp <directory>` will only work if `<directory>` is empty. The workaround for this is recursion, thankfully we don't have to write any recursive algorithms or code, we just have to use it. `scp -r` assists in copying a directory by probing it and all of its subdirectories to copy them.  
Breaking down a common, practical example:  
`scp -r . <username>@ieng6.ucsd.edu~/<directory>`  
`scp -r` has already been explained.  
After that comes the path of the source directory. In this case, the current working directory is copied because of the `.` operator.  
`<username>@ieng6.ucsd.edu~/` is the remote destination of the contents being copied.  
`<directory>` is the name of the new directory that is created and where the contents will be copied onto the remote ssh.  