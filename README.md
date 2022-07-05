# OS_threads
Operating systems

In this mini-project I implemented a multiprocess filesystem search program.

The implementation includes important multithreading concepts such as parallel programing, 
locks (mutex and condition variables) and signals. 
In addition, I learned about filesystem system calls such as opendir, readdir and stat,
using them in my implementation.

The program searches a directory tree for files whose name matches some search term.
The program receives a directory D and a search term T, and finds every file
in D’s directory tree whose name contains T. The program parallelizes its work using threads.
Specifically, individual directories are searched by different threads.

Run this to compile:
gcc -O3 -D_POSIX_C_SOURCE=200809 -Wall -std=c11 -pthread pfind.c

Command line arguments:
1. Search root directory (search for files within this directory and its subdirectories).
2. Search term (search for file names that include the search term).
3. Number of searching threads (assumes a valid integer greater than 0).
