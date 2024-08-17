# Minishell

This project is a simple implementation of a basic command line in C.

## Description

This simple command line is capable of the following:
- Displays a prompt when waiting for a new command.

- Has a working history.

- Searches and launches the right executable (based on the PATH variable or using a relative or an absolute path).

- Does not interpret unclosed quotes or special characters which are not required by the subject such as \ (backslash) or ; (semicolon).

- Handles ’ (single quote) which should prevent the shell from interpreting the metacharacters in the quoted sequence.

- Handles " (double quote) which should prevent the shell from interpreting the metacharacters in the quoted sequence except for $ (dollar sign).

- Handles redirections:
	--- < should redirect input.
	--- > should redirect output.
	--- << should be given a delimiter, then read the input until a line containing the delimiter is seen. However, it doesn’t have to update the history!
	--- >> should redirect output in append mode.

- Handles pipes (| character). The output of each command in the pipeline is connected to the input of the next command via a pipe.

- Handles environment variables ($ followed by a sequence of characters) which should expand to their values.

- Handles $? which should expand to the exit status of the most recently executed foreground pipeline.

- Handles ctrl-C, ctrl-D and ctrl-\ which should behave like in bash in interactive mode:
	--- ctrl-C displays a new prompt on a new line.
	--- ctrl-D exits the shell.
	--- ctrl-\ does nothing.

- The following builtins are also reimplemented as per the subject's requirements:
	--- echo with option -n
	--- cd with only a relative or absolute path
	--- pwd with no options
	--- export with no options
	--- unset with no options
	--- env with no options or arguments
	--- exit with no options

## Usage

- Clone the repository:
	```
		git clone https://github.com/ibenhoci/minishell
	```
- Build the project:
	```
		make
	```
- Run the project:
	```
		./minishell
	```
- Have fun!