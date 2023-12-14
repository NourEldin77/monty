# The Monty Project

The Monty Project is an interpreter for a unique stack-based language called Monty.

## Overview

	The interpreter accepts Monty bytecode as input and outputs the result to stdout. Error messages are printed on stderr.

## Usage
```bash
monty <file>
```
- **file**:Path to the file containing Monty bytecode.

If the user does not provide any file or provides more than one argument to the program, the following error message will be printed, followed by a new line, and the program will exit with the status `EXIT_FAILURE`:

If, for any reason, it's not possible to open the specified file, the following error message will be printed, followed by a new line, and the program will exit with the status EXIT_FAILURE:

```bash
Error: Can't open file <file>
```
where `<file>` is the name of the file.

If the file contains an invalid instruction, the following error message will be printed, followed by a new line, and the program will exit with the status `EXIT_FAILURE`:

```bash
L<line_number>: unknown instruction <opcode>
```
where `<line_number>` is the line number where the instruction appears. Line numbers always start at 1.

## Execution

The Monty program runs the bytecodes line by line and stops if:

- It executed properly every line of the file.
- It finds an error in the file.
- An error occurs.

If the program can't allocate more memory using malloc, the following error message will be printed, followed by a new line, and the program will exit with status `EXIT_FAILURE`:

```bash
Error: 'malloc failed'
```
Note: The program must use malloc and free and is not allowed to use any other function from man malloc (realloc, calloc, ...).


