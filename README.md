# LightGrep Compiler

**LightGrep** is a lightweight text search tool built with JavaCC that allows you to search for patterns in a text file using regular expressions. It mimics the basic functionality of the UNIX `grep` command but is implemented entirely in Java.

## Features
- **Regular Expression Matching:** Supports basic regular expressions to search for patterns in text files.
- **Simple Usage:** Specify a regular expression and a file name, and LightGrep will display all lines that match the expression.

## Prerequisites
- **Java Development Kit (JDK):** Ensure that you have JDK installed on your system.
- **JavaCC:** JavaCC (Java Compiler Compiler) is required to compile the grammar used by LightGrep.

## Installation

1. **Clone the Repository:**

2. **Compile the JavaCC Grammar:**
   ```bash
   javacc LightGrep.jj
   ```

3. **Compile the Java Source Files:**
   ```bash
   javac *.java
   ```

4. **Create the Executable Script:** Make sure `lightGrep.sh` is executable. If not, run:
   ```bash
   chmod +x lightGrep.sh
   ```

## Usage

To use LightGrep, run the following command from the terminal:

```bash
./lightGrep.sh "expressionRationelle" nomFichier
```

- `expressionRationelle`: The regular expression you want to search for (e.g., "abc" or "a*").
- `nomFichier`: The name of the text file you want to search in (e.g., test.txt).

### Example Usage

**Basic Usage:**

```bash
./lightGrep.sh "abc" test.txt
```

This command will print all lines in `test.txt` that contain the string `abc`.

**Pattern with Repetitions:**

```bash
./lightGrep.sh "a*" test.txt
```

This will match lines with zero or more occurrences of the letter 'a'.

## Notes

- If the pattern is not found or if there's an error, the script will return an appropriate message.
- Be cautious with your regular expressions, as certain patterns might cause the script to be suspended, requiring you to adjust the expression or file content.
```
