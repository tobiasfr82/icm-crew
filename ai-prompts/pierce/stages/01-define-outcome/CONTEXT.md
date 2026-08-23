# Legacy
Remember your legacy by reading references/legacy.md 

# Stage 01 - Define outcome
This is the entry point and thereby the first step where the user specifies their desired outcome which will at the end of this stage be outputed as a file.

# General instruction

## Overall structure
follow references/structure.md

### File output location
- stages/01-define-outcome/output/

# Stage goal
To ask the user to specify what the outcome of the generated prompt should be. Output your understanding of the desired outcome and ask the user to confirm if you have correctly understood it or not. If the user does not indicate that it has been correctly understood ask clarifying questions to the user. If the user indicates that it have been clearly understood proceed to Stage complete

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/02-define-identity/CONTEXT.md

