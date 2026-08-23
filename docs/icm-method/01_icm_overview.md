# ICM Overview - core concepts
ICM is an acronym for interpretable context methodology. The methodology was created by Jake Van Clief who released a paper on the methodology: [2603.16021 Interpretable Context Methodology: Folder Structure as Agentic Architecture ](https://arxiv.org/abs/2603.16021)

## Effort vs output
Eduba states that there are three levels of AI use. Depending on which level is being implemented the effort vs output or effort vs impact can change drastically. 

### Level 1 - Chat
- most of usage today
Level 1 is where no system and no verification is implemented. It's the normal chat with AI experience most of use and are familiar with. ex. open ChatGPT, ask a question, copy the answer to where it needs to go. The effort you need to put in to get some output is low. However the impact of the output you get is weak, not huge. In order to get better impact of the output you need to have longer and longer conversations needing multiple chats, saved prompts, tone style etc. This is where prompt libraries, sharing of prompts etc. originated from.

### Level 2 - Skills
- sprint target
- Explainable to colleagues. You know what the tool is good at and what it is not. 

Skills is an example of level 2. You or somebody else took the time to figure out the prompts necessary to get the impact of the output that was desired and put it in a way that is highly reusable. The order it should be run in. Then skills evolved where you only need certain part of skills at a certain time. We don't want to overload the context window and we eventually want to start developing automations. 

Then as workflows and usecases grow and mature this is extended further via the help of skill definitions. so that AI can start to run itself by handling the creating things by using specialized defined markdown files called skills, or take actions ex running python scripts. The output needs to be determanistic in nature as in the same reliable output every time. 

If all of this can be defined in a single prompt this can by uploaded and sent in the correct order this is where skills come from.
Hundreds of skills are available today to use, draw inspiration from or even to serve as templates for creating your own skills.

### Level 3 - Structure
- requires level 2 foundations
Taking multiple skills, multiple prompts, maybe even multiple ai models and linking them together in cohesive workflows organized by a supporting natural directory structure.

# Grounded in discussion and dialogue
All level 1, level 2 and level 3 components all originate from discussion and dialogue in level 1.

Ex.

| Use case | Level 1 Copy & paste | Level 2 structured | Level 3 integrated workflow |
|---|---|---|---|
| Writing & drafting | Paste prompt into ChatGPT, copy the output. | Refined prompt with brand-tone guide, verify against TOV standards. | Auto-draft from structured brief. Human edits only. |
| Code review | Ask AI to explain a function. | AI first-pass review against team rubric, human signs off. | Automated PR review pipeline with HITL checkpoint. |
| Data reporting | Ask ChatGPT to summarize a dataset. | Structured prompt with schema context, verify numbers against source. | Auto-generated compliance reports with human approval step. |

## How it fits together from level 1 to level 3
In level one you discuss with AI, test out and finalize your prompts. You figure out which prompts to run in what order to achieve the output impact you are looking for. This require additional structure and organization which is level 2 where your structure your prompts, maybe even define them in skillsets, starting directory structure to support what you are trying to achieve.

Naturally this leads to level 3 where you also make bigger use of AI's ability to navigate your structure enabling AI to figure out what context to use and what skills and ability to use automatically based on what you either adhoc communicate to it or as part of a workflow producing the repeatable output impact that you designed.

Every process from level 1 to level 3 is transparent and inspectable to you as they are all defined in text markdown files. Including the output from AI if you designed it that way. Regardless if it's code review, a blog post draft or some other deliverable.

This is all driven by dialogue and conversations having the structure and the intent we are looking for is all carried through the conversation. All the way from developing concepts to asking for defined workflow input and help for troubleshooting functionality and so on. It also lends itself to use actual voice to steer the AI as well.


