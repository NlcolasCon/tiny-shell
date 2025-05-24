# tiny-shell

A lightweight command-line shell implemented in C, supporting:

- **Basic command execution**  
- **Input/output redirection** (`<` and `>`)  
- **Pipelines** (`|`)  

This project demonstrates process creation, `exec`, `fork`, `pipe`, and file descriptor manipulation in C.

## Features

1. **Execute simple commands** like `/bin/ls` or `echo hello`.  
2. **I/O Redirection**: e.g. `echo "hi" > out.txt`, `cat < out.txt`.  
3. **Pipelines**: e.g. `ls | sort | uniq | wc`.  
4. **Error handling** on failed `exec`, `open`, `pipe`, etc. :contentReference[oaicite:0]{index=0}


## Build & Run

```bash
# Compile
gcc tsh.c -o tsh

# Non-interactive test mode using tests/t.sh
./tsh < t.sh

# Or run interactively:
./tsh
tsh$ ls | sort | uniq > out.txt
