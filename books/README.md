To create a file, please go to your commandline and enter:

    bookmanager filename.yaml get

When issuing this command a *directory dest* is created in which the book
is compiled. If you run multiple processes at the same time it is best
to create a new directory for that process, copy the yaml file into it,
and then run the bookmanager command inside this unique directory.

This way they do not interfere with each other.

    mkdir NEWDIR
    cp filename.yaml NEWDIR
    cd NEWDIR
    bookmanager filename.yaml get

the epub witll be in `NEWDIR/dest/*.epub`

The filename of the epub file is specified within the yaml file

In python:

    import os

    filename="sample.yaml"
    os.system(f"bookmanager {filename} get")
    
