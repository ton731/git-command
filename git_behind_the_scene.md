### What is in .git?
1. objects/
    - The objects directory contains all the repo files.
    - This is where Git stores the backups of files, the commit in repo, and more.
    - The files are all compressed and encrypted.
2. config
    - The configuration file.
3. HEAD
    - A text file that keeps track of where HEAD points.
4. index
    - A binary file that contains a list of the files the repo is tracking. 
    - It does not store the content of the file. It only contains references of the files.
5. refs/
    - There's heads directory in it, and refs/heads contains one file per branch in the repo.


### Hashing
- SHA-1
    - Git uses SHA-1 hashing function
    - SHA-1 always generates 40-digit hexadecimal numbers
- Git Database
    - Git is a **key-value data store**. We can insert any kind of content into Git repo, and Git will hand us back an unique key that we can later use to retrieve that content.
    - These keys that we get back are SHA-1 checksums.
- `git hash-object <flie>`
    - Take some data, store in our .git/objects directory and give us back the unique SHA-1 hash that refers to that data object.
    - In this simplest form, git simply return the unique key that WOULD be used to store our object. But it does not actually store anything.
- `echo "hello" | git hash-object --stdin`
    - It will hash the word "hello"
- `echo "hello" | git hash-object --stdin -w`
    - Rather than simply outputting the key that git will store our object under, we can use the -w option to tell git to write the object to the database.
- `git cat-file -p <object-hash>`
    - Now that we have data stored in our Git object database, we can try retrieving it using the git cat-file command.
    