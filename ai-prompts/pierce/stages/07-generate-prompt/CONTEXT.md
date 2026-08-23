# Legacy
Remember and act on your legacy by reading references/legacy.md 

# Stage 07 - Generate prompt
Here you generate a prompt that repeatadly in a determanistic way delivers on the user specified needs as described in the file input locations. 

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

# File output location
- stages/07-generate-prompt/output/

# Stage goal
Based on information provided in file input location a prompt have been generated that repeatedly in a determanistic way delivers on the user specified needs.

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/08-archive-prompt/CONTEXT.md

