# Using ICM with multiple LLM's
The preferred LLM to use with ICM in the ICM community is Claude models. However ICM is not Claude specific and can be tailor to work with other LLMs. 

The first entry point file that you will create is a CLAUDE.md or AGENTS.md file. You don't need to worry what to put it in. What you need to know right now is that Claude models automatically recognise a CLAUDE.md file and pulls instructions from it. Other LLM models do not recognise CLAUDE.md automatically and are more used to AGENTS.md file. 

Both CLAUDE.md and AGENTS.md serve the same purpose. They are the entry point for the AI/LLM to get it's initial understanding of your project. It's the first thing that gets loaded in the ICM method. You can read more about the entry point file in 03_icm_entry_point.md

This might sound complicated however it's very simple. 

- If you are using Claude models. Great just follow the ICM method and work with CLAUDE.md file.
- If you use other LLMs, or you are just used to working with AGENT.md you can simply create a CLAUDE.md and in there write one line with an instruction to read AGENT.md instead.
- If you don't use Claude feel free to just rename CLAUDE.md to AGENT.md as their functions are the same. Claude just expects a CLAUDE.md file over an AGENT.md file.

## Simple example of CLAUDE.md that instructs AI to read AGENT.md
go to "c:\<path to your your project directory>\AGENT.md" and follow instructions.

## Advanced example
If you use a linux based OS you can create a symlink between CLAUDE.md pointing it towards the AGENT.md file. 

This is an advanced setup and if it doesn't make sense to you don't worry about it. Just follow the simple example. I'm an advanced user and can setup symlinks on linux and I prefer using the simple method so you don't loose anything by keeping it simple.

# Multiple LLM's might get different results
When you use multiple LLM's with the ICM method just remember that your results might differ. Experiment and improve as you go until you get the desired output impact that you are looking for.

