Vow-fs [![Build Status](https://secure.travis-ci.org/dfilatov/vow-fs.png)](http://travis-ci.org/dfilatov/vow-fs)
======

[Vow](https://github.com/dfilatov/jspromise)-based file I/O for Node.js

Getting Started
---------------
You can install Vow-fs using Node Package Manager (npm):

    npm install vow-fs

````javascript
var fs = require('vow-fs');
````

API
---
####read(path, [encoding=utf8])####
Returns a promise for the file's content at a given ````path````.
####write(path, data, [encoding=utf8])####
Writes ````data```` to file at a given ````path````. Returns a promise for the completion of the operation.
####append(path, data, [encoding=utf8])####
Appends````data```` to file's content at a given ````path````. Returns a promise for the completion of the operation.
####remove(path)####
Removes a file at a given ````path````. Returns a promise for the completion of the operation.
####copy(sourcePath, targetPath)####
Copies a file from ````sourcePath```` to ````targetPath````. Returns a promise for the completion of the operation.
####move(sourcePath, targetPath)####
Moves a file or directory from ````sourcePath```` to ````targetPath````. Returns a promise for the completion of the operation.
####stats(path)####
Returns a promise for the metadata about the given ````path```` as a [Stats](http://nodejs.org/api/fs.html#fs_class_fs_stats) object.
####exists(path)####
Returns a promise for whether the given ````path```` exists.
####link(sourcePath, targetPath)####
Creates a hard link from the ````sourcePath```` to ````targetPath````.
####symLink(sourcePath, targetPath, [type=file])####
Creates a symbolic link from the ````sourcePath```` to ````targetPath````.
####chown(path, uid, gid)####
Changes the owner of a given ````path````.
####chmod(path, mode)####
Changes the mode of a given ````path```` to ````mode````.
####absolute(path)####
####isFile(path)####
Returns a promise for whether the given ````path```` is a file.
####isDir(path)####
Returns a promise for whether the given ````path```` is a directory.
####isSocket(path)####
Returns a promise for whether the given ````path```` is a socket.
####isSymLink(path)####
Returns a promise for whether the given ````path```` is a symbolic link.
####listDir(path)####
Returns a promise for a list of files and directories in directory at the given ````path````.
####makeDir(path, [mode=0777], [failIfExist=false])####
Makes a directory at a given ````path```` and any necessary subdirectories (like ````mkdir -p````). Returns a promise for the completion of the operation.
####removeDir(path)####
Recursively removes a directory at a given path (like ````remove -rf````). Returns a promise for the completion of the operation.
