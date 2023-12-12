# Shell Library

This library provides a collection of reusable shell functions and utilities for your scripts. It's designed to be self-contained and easy to integrate into your existing projects.

Files:

    logging.sh: Provides functions for logging messages with different levels (info, error, debug).
    common.sh: Contains several common shell functions you might find useful.
    colors.sh: Maps color names to their ANSI escape codes for formatting output.

Logging Functions:

    log::info: Logs an informative message.
    log::err: Logs an error message.
    log::debug: Logs a debug message (only shown if debug mode is enabled).

## Usage:

### Source the library files:


```shell
# Source individual files
source <(curl https://raw.githubusercontent.com/YojimboSecurity/shell-libs/main/logging.sh)
source <(curl https://raw.githubusercontent.com/YojimboSecurity/shell-libs/main/common.sh)
source <(curl https://raw.githubusercontent.com/YojimboSecurity/shell-libs/main/colors.sh)

# Or source the entire library directory
source <(curl https://raw.githubusercontent.com/YojimboSecurity/shell-libs/main/shell-libs.tar.gz | tar -xzf -)
```

### Use the functions:

#### Use logging
```shell
log::info "Starting script..."
# Do something
log::debug "Variable value: $my_variable"
if [ $? -ne 0 ]; then
  log::err "An error occurred!"
fi
```

##### Use common functions

```shell
# returns 0 or true
common::string_contains "this is a test" "test" 
```

##### Use colors
```shell
echo "This is red" "$(colors::red)"
```

## Features:

    Modular: Each file focuses on a specific functionality, making it easy to include only what you need.
    Simple: Functions are straightforward and easy to use.
    Clean: Code is well-formatted and documented.
    URL-based sourcing: Allows easy integration from any environment.
    Color support: Enhance your scripts with ANSI colors.

## Contributions and Feedback:

We welcome contributions and feedback to improve this library. Feel free to fork the repository at https://github.com/YojimboSecurity/shell-libs and submit pull requests.

We hope this library makes your shell scripting more efficient and enjoyable!
