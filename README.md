# bash-scripting

# Bash Scripting Syntax

This guide provides an overview of basic syntax, constructs and examples used in Bash scripting.

## Overview

Bash (Bourne Again SHell) is a command language interpreter for Unix-based systems. Bash scripting allows users to automate tasks by writing scripts containing commands that the shell can execute.

## Script Creation

To create a Bash script:
1. Use a text editor like Vim, Nano, or Sublime Text.
2. Start the script with `#!/bin/bash` to indicate it's a Bash script.

Example:
```bash
#!/bin/bash
# This is a simple Bash script
echo "Hello, World!"
```
## Comments

Comments in Bash scripts start with # and are used for adding explanatory notes.
```bash
# This is a comment in a Bash script
```

## Variables

Assign values to variables using =. No spaces are allowed between the variable name, the =, and the value.
```bash
NAME="John"
AGE=30
```

To access the value stored in a variable, prefix it with a $.
```bash
echo "Name: $NAME"
```

## Input/Output

- echo: Used to print text or variables to the terminal.
- read: Accepts user input and assigns it to a variable.
```bash
echo "Enter your name:"
read USER_INPUT
echo "Hello, $USER_INPUT"
```

## Conditional Statements

If-Else Statements
```bash
if [ condition ]; then
    # Statements
elif [ condition ]; then
    # Statements
else
    # Statements
fi
```

Example:
```bash
AGE=25

if [ "$AGE" -lt 18 ]; then
    echo "You're a minor."
elif [ "$AGE" -ge 18 ] && [ "$AGE" -lt 65 ]; then
    echo "You're an adult."
else
    echo "You're a senior citizen."
fi
```

## Loops

For Loop
```bash
for ITEM in item1 item2 item3; do
    # Statements
done
```

Example:
```bash
FRUITS="Apple Orange Banana"

for FRUIT in $FRUITS; do
    echo "Fruit: $FRUIT"
done
```

While Loop
```bash
while [ condition ]; do
    # Statements
done
```

Example:
```bash
COUNT=1

while [ $COUNT -le 5 ]; do
    echo "Count: $COUNT"
    ((COUNT++))
done
```

## Functions

Declare functions using the function keyword:
```bash
function myFunction() {
    # Statements
}
```

Example:
```bash
function greet() {
    echo "Hello, $1!"
}

greet "Alice"
```

Conclusion

This provides an overview of fundamental Bash scripting syntax and structures, offering just a glimpse into its potential. Bash scripting's versatility empowers the automation of diverse tasks within Unix-based systems, showcasing its robust capabilities.
