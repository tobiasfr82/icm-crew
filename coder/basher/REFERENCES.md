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

## Relevant links


## Notes
