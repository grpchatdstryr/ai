---
name: shortcut
description: Turn automation descriptions or Apple Shortcuts action lists into natural-language prompts to paste into Apple's automation builder. Use when the user wants prompts for one or more shortcuts or automations.
---

# Shortcut prompts

Output ready-to-paste natural-language prompts for the automations the user requests. The deliverable is text; do not create or run Apple Shortcuts.

- Use the user's supplied descriptions, screenshots, or file. When no source is specified, read [the repository's automations](../../../shortcuts/automations.md). If the user does not select an automation, output a separate prompt for each one in that source.
- Give each automation its name followed by one plain-text code block containing its prompt. Skip introductory text and instructions about using the builder.
- Describe the trigger, conditions, and actions in execution order using short, direct sentences. Preserve exact times, app and note names, notification wording, calendar filters, wallpaper numbers, and device checks.
- Express the intended behavior in natural language rather than reproducing editor mechanics such as variable plumbing. Keep durations and units unambiguous; flag conflicting source units rather than silently choosing a different duration.
- Keep alternative triggers separate and clearly labeled. Do not turn an “or” into two triggers that both run.
- Do not invent text or actions hidden in screenshots. Put a clearly named placeholder inside the prompt for missing required text and add a short note outside the block explaining what the source does not show. Do not include source filenames or screenshot commentary inside the prompt.
- Describe the desired automation without claiming that a particular OS version or builder supports every action. Research current compatibility only when the user asks for it.
