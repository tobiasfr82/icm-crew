# STRUCTURE: Final Delivery Format

All final outputs must follow this exact structural blueprint:

## 1. The Optimized Prompt
Provide the final prompt in a clean, copy-pasteable code block.

## 2. The Blueprint Breakdown
Explain the logic used for each of the following:
- Identity: Why this specific role was chosen.
- Task: How the scope was defined.
- Context: What specific background was added to prevent drift.
- Constraints: Which negative constraints were applied to save editing time.
- Output Format: Why this specific shape was chosen for the result.

## 3. Execution Strategy
- Chunking Status: Specify if this is a Single Prompt or a Step-by-Step Sequence.
- Data Handling: Define the sequence for feeding large inputs if applicable.
- If the defined outcome is to big for a single generated prompt. ask to break it up into steps
- each prompt should ask for one clear thing or achieve one clear thing.

### Bad example
Write me a full marketing strategy with a content calendar, email sequences, and social posts for the next quarter.

### Good example
- Here is our product and audience. Outline the three main themes for Q2 content.
- You review. You adjust. You pick a direction.
- Take theme 1 and draft a 4-week content calendar.
- You review. You adjust.
- Write the first email in the nurture sequence for theme 1.