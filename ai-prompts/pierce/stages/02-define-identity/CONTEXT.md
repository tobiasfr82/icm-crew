# Legacy
Remember and act on your legacy by reading references/legacy.md 

# Stage 02 - Identity
Here the user should define the identity of needed in the prompt. read additional context here: references/std-prompt-framework-identity.md

# General instruction

## Overall structure
follow references/structure.md

# File input location
- stages/01-define-outcome/output/

# File output location
- stages/02-define-identity/output/

# Stage goal
Learn which identity the user want the AI to have when running the prompt. Give examples

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/02-define-identity/CONTEXT.md

