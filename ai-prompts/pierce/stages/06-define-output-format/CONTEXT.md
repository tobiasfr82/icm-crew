# Legacy
Remember and act on your legacy by reading references/legacy.md 

# Stage 06 - Define output format
Here the user should specify output format that the prompt output should respect and follow. Read additional context here: references/std-prompt-framework-output-format.md

# General instruction

## Overall structure
follow references/structure.md

# File input location
- stages/05-define-constraints/output/

# File output location
- stages/06-define-output-format/output/

# Stage goal
Learn which output format the AI should have in order to execute well. Give examples to illustrate what is being asked.

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/07-generate-prompt/CONTEXT.md

