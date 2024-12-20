![alt text](./.img/loading.jpg)
---
## spix - CLI Spinner 

spix is a command line (CLI) tool written in C++ that displays an animated spinner while a background process is running.  It is useful for visually indicating that a task is in progress, especially if the task takes a considerable amount of time.

## Install

`git clone https://github.com/VictorH028/spix && cd  spix`
`make`

## Usage
    
Command line:
```
Usage: spix [options]

Options:
  -h, --help            show this help message and exit
  -t TEXT, --text=TEXT  Text to show
  -i INT, --interval=INT
                        Interval in milliseconds
  -s STRING, --symbols=STRING
                        Symbols the spinner
  -p COMMAND, --process=COMMAND
                        Command to execute
  -l, --list_symbols    List of symbols
```

**It also has an integrated manual.**
`man spix`

> [!NOTE]
> **Predefined Symbol**
> > circleHalves: ◐◓◑◒

## Example 

**Show a spinner with custom text:**
```bash
spix -t "loading..." -p "sleep 3"
```

## Programming

### Use as **python** module:

- Requirement 

```sh 
pip install pybind11
```

- Compilation

```
make python
```
#### Example

```py
import spinners
import time

# Create a Spinner object
s = spinners.Spinner()

# Set.textnand)symbols
s.set_text("Cargando...")
s.set_symbols("dots")

#Start and stop the spinner
s.start()
time.sleep(5)
s.stop()
```

## Contribute

If you would like to contribute to this project, please fork the repository and submit a pull request.

## Reference 

- [optparce](https://github.com/myint/optparse)
