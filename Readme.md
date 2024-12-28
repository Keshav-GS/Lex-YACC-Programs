# Lex and YACC Programs Repository

This repository contains 12 programs written using Lex and YACC, labeled as `1a`, `1b`, `2a`, `2b`, `3a`, `3b`, `4a`, `4b`, `5`, `6`, `7`, and `8`. Each program demonstrates specific functionalities and parsing tasks, with some involving both Lex and YACC.

## Repository Structure

```
lex-yacc-programs/
│
├── 1a/  # Program 1a
│   ├── 1a.l  # Lex file to count words, lines, characters, and whitespaces
│   └── README.md  # Specific instructions for this program
│
├── 1b/  # Program 1b
│   ├── 1b.l  # Lex file for character recognition
│   ├── 1b.y  # YACC file for validating input grammar
│   └── README.md  # Specific instructions for this program
│
├── 2a/  # Program 2a
│   ├── 2a.l  # Lex file for counting numbers and fractions
│   └── README.md  # Specific instructions for this program
│
├── 2b/  # Program 2b
│   ├── 2b.l  # Lex file for tokenizing arithmetic expressions
│   ├── 2b.y  # YACC file for evaluating arithmetic expressions
│   └── README.md  # Specific instructions for this program
│
├── 3a/  # Program 3a
│   ├── 3a.l  # Lex file for removing comments from a C program
│   ├── 3a_ip.txt  # Input file with comments in C code
│   ├── 3a_op.txt  # Expected output with comments removed
│   └── README.md  # Specific instructions for this program
│
├── 3b/  # Program 3b
│   ├── 3b.l  # Lex file to tokenize for loops, identifiers, and numbers
│   ├── 3b.y  # YACC file for parsing nested for loops
│   └── README.md  # Specific instructions for this program
│
├── 4a/  # Program 4a
│   ├── 4a.l  # Lex file to process keywords, identifiers, and operators
│   ├── 4a_ip.txt  # Input file with arithmetic expressions
│   └── README.md  # Specific instructions for this program
│
├── 4b/  # Program 4b
│   ├── 4b.l  # Lex file to tokenize if statements and expressions
│   ├── 4b.y  # YACC file for parsing nested if statements
│   └── README.md  # Specific instructions for this program
│
├── 5/  # Program 5
│   ├── 5.l  # Lex file for tokenizing type declarations
│   ├── 5.y  # YACC file for counting total variables declared
│   ├── 5_input.txt  # Input file with type declarations
│   └── README.md  # Specific instructions for this program
│
├── 6/  # Program 6
│   ├── 6.l  # Lex file for tokenizing mathematical expressions
│   ├── 6.y  # YACC file for generating three-address and quadruple code
│   └── README.md  # Specific instructions for this program
│
├── 7/  # Program 7
│   ├── 7.l  # Lex file for tokenizing C program components
│   ├── 7.y  # YACC file for parsing and validating C programs
│   ├── 7_input.txt  # Input file with a sample C program
│   └── README.md  # Specific instructions for this program
│
├── 8/  # Program 8
│   ├── 8.l  # Lex file for tokenizing C programs for assembly output
│   ├── 8.y  # YACC file for generating assembly-like code
│   └── README.md  # Specific instructions for this program
```

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

