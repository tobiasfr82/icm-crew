# References

# General

The principles of Clean Code apply

Always use long parameter notation when available. This makes the script more readable, especially for lesser known/used commands that the user don’t remember all the options for.

## Avoid
    rm -rf -- "${dir}"

## Good
      rm --recursive --force -- "${dir}"

# Avoid

    cd "${foo}"
    [...]
    cd ..

# Good

    (
        cd "${foo}"
        [...]
    )



## Examples of good work
Here is an example of a good structured bash script. Not all of these components are required in all bash scripts. Use it as example of good structure and good work.

#!/bin/bash

# ==============================================================================
# SCRIPT METADATA
# Name:         system_backup.sh
# Description:  A structured example script to automate backups and logging.
# Author:       Your Name
# ==============================================================================

# --- CONFIGURATION ---
# Exit immediately if a command exits with a non-zero status
set -e 

# Treat unset variables as an error and exit immediately
set -u 

# Global Variables
BACKUP_DIR="/var/backups"
LOG_FILE="/var/log/system_backup.log"

# --- FUNCTIONS ---

# Print formatted logging messages
log_message() {
    local timestamp
    timestamp=$(date "+%Y-%m-%d %H:%M:%S")
    echo "[${timestamp}] $1" | tee -a "$LOG_FILE"
}

# Perform the backup
perform_backup() {
    log_message "Starting backup process..."
    
    # Check if directory exists
    if [ ! -d "$BACKUP_DIR" ]; then
        log_message "Error: Target directory ${BACKUP_DIR} does not exist."
        exit 1
    fi

    # Execute backup command here
    log_message "Backup completed successfully!"
}

# --- MAIN EXECUTION ---

# Ensure the script is run as root
if [ "$EUID" -ne 0 ]; then
    echo "Error: This script must be run as root." >&2
    exit 1
fi

# Parse command line arguments
if [ "$#" -eq 1 ]; then
    BACKUP_DIR="$1"
fi

perform_backup

exit 0

# Best Practise

## Color definition

### ALWAYS Reset your colors
If you do not reset the color at the end of your string, the color will bleed into the user's terminal prompt after the script exits. Always append your reset variable (${NC}) to the end of colored strings.

Ex. echo -e "${GREEN}Database backup completed successfully.${NC}"

* (Note: Use echo -e to enable interpretation of backslash escapes, or prefer printf for better portability).

### Prefer tput for Maximum Portability
While \\033[...m works on most modern terminals (like the ones in Pop!_OS or standard Ubuntu), the most robust and POSIX-compliant way to handle terminal colors is using the tput command. tput reads the terminal database (terminfo) and outputs the exact correct escape sequence for the current terminal.

ex.
# Using tput
readonly RED=$(tput setaf 1)
readonly GREEN=$(tput setaf 2)
readonly YELLOW=$(tput setaf 3)
readonly BLUE=$(tput setaf 4)
readonly BOLD=$(tput bold)
readonly RESET=$(tput sgr0)

printf "%s%s%s\\n" "${BOLD}${BLUE}" "Starting system update..." "${RESET}"

### Handle Redirection and Piping (The "Is it a Terminal?" Check)
If a user pipes your script's output to a file (./script.sh > log.txt), ANSI color codes will be written to the file as ugly garbled characters (e.g., ^[[0;32mSuccess).

Best Practice: Dynamically disable colors if the standard output (stdout) is not connected to an interactive terminal.

ex.
# Check if stdout is a terminal
if [ -t 1 ]; then
    RED=$(tput setaf 1)
    GREEN=$(tput setaf 2)
    YELLOW=$(tput setaf 3)
    RESET=$(tput sgr0)
else
    # If output is piped or redirected, leave variables empty
    RED=""
    GREEN=""
    YELLOW=""
    RESET=""
fi

echo "${YELLOW}This will only be yellow in a terminal.${RESET}"

### Recommended Boilerplate Script
Here is a robust, production-ready snippet you can drop into the top of your scripts, utilizing printf for safe formatting and handling piped outputs perfectly.

#!/usr/bin/env bash

# -----------------------------------------------------------------------------
# Color Setup (Safe for logs & pipes)
# -----------------------------------------------------------------------------
setup_colors() {
    if [[ -t 2 ]] && [[ -z "${NO_COLOR-}" ]] && [[ "${TERM-}" != "dumb" ]]; then
        # -t 2 checks stderr (standard for logging). Use -t 1 for stdout.
        # NO_COLOR allows users to disable colors via environment variable.
        NOFORMAT='\\033[0m' RED='\\033[0;31m' GREEN='\\033[0;32m' ORANGE='\\033[0;33m' \\
        BLUE='\\033[0;34m' PURPLE='\\033[0;35m' CYAN='\\033[0;36m' YELLOW='\\033[1;33m'
    else
        NOFORMAT='' RED='' GREEN='' ORANGE='' BLUE='' PURPLE='' CYAN='' YELLOW=''
    fi
}

setup_colors

# -----------------------------------------------------------------------------
# Logging Helper Functions
# -----------------------------------------------------------------------------
msg() {
    echo >&2 -e "${1-}"
}

info() {
    msg "${BLUE}[INFO]${NOFORMAT} ${1-}"
}

success() {
    msg "${GREEN}[SUCCESS]${NOFORMAT} ${1-}"
}

warn() {
    msg "${YELLOW}[WARNING]${NOFORMAT} ${1-}"
}

die() {
    msg "${RED}[ERROR]${NOFORMAT} ${1-}"
    exit 1
}

# --- Usage Example ---
info "Connecting to production server..."
# ... code ...
warn "Latency is higher than expected."
# ... code ...
success "Deployment completed."
# die "Failed to start service." 

Summary Checklist

    [ ] Use semantic mapping (Red = Error, Green = Success).  

    [ ] Assign color codes to read-only variables at the top of the script.  

    [ ] Always append a RESET or NO_COLOR code at the end of the line.  

    [ ] Use [ -t 1 ] to disable colors when output is redirected to files.  

    [ ] Respect the NO_COLOR environment variable standard.
    """

file_path = "bash_colors_best_practices.md"
with open(file_path, "w", encoding="utf-8") as f:
f.write(markdown_content)

print(f"Successfully generated {file_path}")

## Relevant links


## Notes
