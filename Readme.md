# Lex and YACC Programs Repository

This repository contains 12 programs written using Lex and YACC, labeled as `1a`, `1b`, `2a`, `2b`, `3a`, `3b`, `4a`, `4b`, `5`, `6`, `7`, and `8`. Each program demonstrates specific functionalities and parsing tasks, with some involving both Lex and YACC.

## Getting Started

### Prerequisites
To build and run the programs, ensure you have the following tools installed:
- `lex` (or `flex`)
- `yacc` (or `bison`)
- A C compiler (e.g., `gcc`)

### Building and Running
For each program:

1. Navigate to the respective directory (e.g., `cd 1a`).
2. Run the following commands:

   #### For Lex files:
   ```bash
   lex <filename>.l
   gcc lex.yy.c -o <output>
   ./<output>
   ```

   #### For YACC files:
   ```bash
   yacc -d <filename>.y
   lex <corresponding Lex file>.l
   gcc y.tab.c lex.yy.c -o <output>
   ./<output>
   ```

## Overview of Programs

### Program 1a
- **1a.l**: Counts the number of words, lines, characters, and whitespaces in the input.

### Program 1b
- **1b.l & 1b.y**: Validates input strings based on defined grammar rules.

### Program 2a
- **2a.l**: Counts positive/negative integers and fractions from the input.

### Program 2b
- **2b.l & 2b.y**: Evaluates arithmetic expressions.

### Program 3a
- **3a.l**: Removes comments from a C program and counts the total number of comments.
- **Input (3a_ip.txt)**: A C program with single-line and multi-line comments.
- **Output (3a_op.txt)**: The same program with all comments removed.

### Program 3b
- **3b.l & 3b.y**: Parses and validates nested `for` loops and counts them.

### Program 4a
- **4a.l**: Processes arithmetic expressions in a C-style code snippet.
  - Counts keywords (`int`, `float`, `char`), identifiers, and operators.
- **Input (4a_ip.txt)**: C code snippet with declarations and arithmetic operations.

### Program 4b
- **4b.l & 4b.y**: Parses and validates nested `if` statements and counts them.

### Program 5
- **5.l & 5.y**: Tokenizes type declarations, identifiers, and arrays, and parses declarations to count total variables.
- **Input (5_input.txt)**: Sample type declarations with variables and arrays.

### Program 6
- **6.l & 6.y**: Tokenizes mathematical expressions with variables and numbers, and generates three-address code and quadruple code for expressions.

### Program 7
- **7.l & 7.y**: Tokenizes components of a C program, ignoring comments, and parses and validates the structure of C programs, including functions and statements.
- **Input (7_input.txt)**: A sample C program demonstrating declarations, statements, and comments.

### Program 8
- **8.l & 8.y**: Tokenizes components for assembly-like code generation and generates assembly-like code for simple C programs with arithmetic and `printf` statements.

## Contributing
Feel free to contribute by opening issues or submitting pull requests to enhance the repository.

## License
This project is open-source and available under the [MIT License](LICENSE).

