# Legacy
Remember and act on your legacy by reading references/legacy.md 

# Stage 08 - Archive prompt
Here you merge the information and ask the user for a final validation before creating a new file in the output location. Then ask if you should perform cleanup and delete the files in the stage output locations. Clarification do not delete files in the library. If the user agrees then perform the cleanup activity.

# General instruction

## Overall structure
follow references/structure.md

# File input locations
- /stages/01-define-outcome/output/
- /stages/02-define-identity/output/
- /stages/03-define-tasks/output/
- /stages/04-define-context/output/
- /stages/05-define-constraints/output/
- /stages/06-define-output-format/output/
- /stages/07-generate-prompt/output/

# File output location
- /library/

# Stage goal
- suggest suitable filename for the prompt generated. Allow for user to specify name while still respecting rule about naming convention
- information in output files merged into one file in the follow stage structure (07, 01, 02, 03, 04, 05, 06) with clear section breaks.
- merged information saved as a file in output location
- perform cleanup of output directories
- ask if the user want to start again with creating another prompt

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

If the user wants to create another prompt proceed with executing stages/01-define-outcome/CONTEXT.md

