---
name: learning-notes
description: Reorganize the user's learning notes across various scopes, based on the given conditions.
disable-model-invocation: true
argument-hint: "\n- \"노트1.md\"\n- \"노트2.md\"...\n\n상세 조건:"
---

## Given Conditions

Existing target notes to reorganize with:$ARGUMENTS

## Confirming Titles and Scopes

### Optional Step: Importance Assessment

**Run this step only if the user has explicitly mentioned '중요성 판단'**

- Setting aside the framing of the context or given notes, briefly reality-check the topics. State what actually matters about them in practice, and whether any of them holds little value for learning.
- Once the user responds, run Step 0 below.

### Step 0: Confirm Each Note's Title and Overview (Its Scope)

- The overview is a line starting with `>` directly below the H1 header. Create one if the note has none, and revise it if needed.
- Keep this step brief; there is not much to decide.
- Once the user confirms, run the per-note processing below, once for each note.

## Per-Note Processing

### Step 1: Propose Header Structures

- Build header structures fresh, or rework the ones the note already has. Propose three candidates, covering only the sections being added or revised.
- Explain the intended direction of each without filling in the content.
- Once the user picks a structure, run Step 2 below.

### Step 2: Fill in Content

- Following the chosen structure, keep existing content as-is or redistribute it.
- Add or revise content in a concise, declarative style.
- When a structural diagram is needed, use Mermaid.
