# Completely Messed Up Filesystem (CMUF)

A project similar to the big list of naughty strings https://github.com/minimaxir/big-list-of-naughty-strings

The idea being to replicate all sorts of intersting filesytem possibilies that your program might run into so that if you are doing file parsing you can debug and step though all the quirks.

Goals

Have a filesystem with a number of special files and directories in it, hidden files, special files (CON for Windows etc..). Each file should have 1 line in it (so we can count the number expected vs found lines).

Also want some some file commands to count the number of files and lines to ensure we have a baseline, something like
```
find ./cmuf/ -not -type d | wc -l
6757
find ./cmuf/ -type f | wc -l
6763
```
  
Which can then be used to determine if your file system parser accounts for every possible situation.
