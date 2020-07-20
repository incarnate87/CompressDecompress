# CompressDecompress
A project using Node.js to perform actions like - viewing structure of a directory (both flat file view and tree view), copying the structure (including all sub-folders and files in that directory) into a json file, and then recreating that directory's structure into an empty folder; based on the command selected by the user.

Firstly, you need to install uniqid module for renaming of files, when they're copied from one directory to another.
For that,
1)Either copy the node_modules folder of this repo in your project directory
                        OR
2) type: npm install uniqid
in terminal

Now, to run the script,
type: node compDecomp help
command in terminal, which brings up a list and format of available commands:
1) node compDecomp view src -f 
(for flat file view)

2) node compDecomp view src -t 
(for tree view)

3) node compDecomp untreefy src dest 
(to copy structure of src directory in a json file in dest and also copy text files with new names in it)

4) node compDecomp treefy src dest 
(here, src will be the same directory where metadata.json was created as a result of running "untreefy" command, and dest should be an empty directory. This command will then recreate the structure of your previous src directory [which you viewed and untreefied earlier] in this new dest directory)

Here, 'src' and 'dest' are complete or relative paths of the source and destination directories being used.

Here, I have created 'dir' directory, which can be initially used as the src in view and untreefy commands (or you may create your own directory structure in a new folder).

For dest part of untreefy command, you'll need to create a new empty folder by yourself and give its path in place of dest part in untreefy command.

And for treefy command, the src will be that folder's path which you created as dest for untreefy.
dest to be used in treefy should be again, a new empty folder's path, where old src directory's structure will be recreated.

There's a demo video included for any help.
