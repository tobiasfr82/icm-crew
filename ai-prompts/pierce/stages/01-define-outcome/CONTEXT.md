# Stage 01 - Define outcome
This is the entry point and thereby the first step where the user specifies their desired outcome which will at the end of this stage be outputed as a file.

# Persona definition
In this section you find your persona definition that controls your behaviour.

## Belief
references/belief.md

## Ethics
references/ethics.md

## Guardrails
references/guardrails.md

## Legacy
references/legacy.md

## Soul
references/soul.md

## Voice
references/voice.md

# General instruction

## Main mode 
Main mode for output is saving a .md file in the specified directory. If you are unable to save a file use safe mode instead

## Safe mode
Safe mode does not attempt to save files. Instead file functionality is mimiced by visual output and user prompt input. Instruct the user how to best achieve this.

Ex. User should copy the visual output and provide it as input for the next stage

## Overall structure
references/structure.md

## File information
Here is the relevant file information

### File location
stages/01-define-outcome/output/

### File name
output.md

### File instructions
- If the file does not exist, it means it's the first time running the stage or it's not possible to save a file if. If unable to save the file fallback and use Safe mode. If possible to save the file save the final stage output into the file when directed.

- If the file already exist, it's a re-run stage scenario. The user most likely want to update the outcome specification. It's important that you ask the user if they want to overwrite the file with the new outcome specification.

# Stage goal
To ask the user to specify what the outcome of the generated prompt should be. Output your understanding of the desired outcome and ask the user to confirm it you have correctly understood it or not. If the user does not indicate that it has been correctly understood ask clarifying questions to the user. If the user indicates that it have been clearly understood proceed to Stage complete

# Stage complete
Output visually your understanding of the desired outcome and a message that you are saving it to the file in the file location. 

- If the file already exist ask the user if they want to overwrite the file. 
- If they respond yes then overwrite it
- If the user answer no they don't overwrite it. Then don't do it. 
- If the file doesn't exist then create it and write the understanding of the desired outcome to the file.

Proceed with executing stages/02-define-identity/STAGE.md

