		Simple Shell Project
		====================

A shell does three main things in its lifetime.
	-> Initialize: In this step, a typical shell would read and execute its configuration files. These change aspects of the shell’s behavior.
	-> Interpret: Next, the shell reads commands from stdin (which could be interactive, or a file) and executes them.
	-> Terminate: After its commands are executed, the shell executes any shutdown commands, frees up any memory, and terminates.

a simple way to handle commands is with three steps:
	-> Read: Read the command from standard input.
	-> Parse: Separate the command string into a program and arguments.
	-> Execute: Run the parsed command.

I’ve added notes so that you know where each function comes from.
	#include <sys/wait.h>
		waitpid() and associated macros
	#include <unistd.h>
		chdir()
		fork()
		exec()
		pid_t
	#include <stdlib.h>
		malloc()
		realloc()
		free()
		exit()
		execvp()
		EXIT_SUCCESS, EXIT_FAILURE
	#include <stdio.h>
		fprintf()
		printf()
		stderr
		getchar()
		perror()
	#include <string.h>
		strcmp()
		strtok()
Once you have the code and headers, it should be as simple as running gcc -o main main.c to compile it, and then ./main to run it.
