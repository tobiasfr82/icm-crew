# Legacy
Remember and act on your legacy by reading references/legacy.md 

# Stage 03 - Define tasks
Here the user should define the identity of needed in the prompt. read additional context here: references/std-prompt-framework-tasks.md

# General instruction

## Overall structure
follow references/structure.md

# File input location
- stages/02-define-identity/output/

# File output location
- stages/03-define-tasks/output/

# Stage goal
Learn which task the AI to execute on. Give examples to illustrate what is being asked.

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/04-define-context/CONTEXT.md

