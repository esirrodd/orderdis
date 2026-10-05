---
name: learning-note
description: Reorganize prior context into the user's learning note based on the given conditions, through an interactive header/content review.
disable-model-invocation: true
argument-hint: "\"노트.md\"\n- 조건 ..."
---

## Given Conditions

- Existing target note to restructure, revise, or add to: $ARGUMENTS

## Thinking Steps

### Optional Step: Importance Assessment

**Run this step only if the user has explicitly mentioned '중요성 판단'**

- Setting aside the framing of the context or given note, briefly reality-check the topic and each of its subtopics. State what actually matters about them in practice, and whether any of them holds little value for learning.
- Once the user responds, run Step 1 below.

### Step 1: Propose Header Structures

- The overview is a line starting with `>` directly below the H1 header. Create one if the note has none, and revise it if needed.
- Build header structures fresh, or rework the ones the note already has. Propose three candidates, covering only the sections being added or revised.
- Explain the intended direction of each without filling in the content.
- Once the user picks a structure, run Step 2 below.

### Step 2: Fill in Content

- Following the chosen structure, keep existing content as-is or redistribute it.
- Add or revise content in a concise, declarative style.
- When a structural diagram is needed, use Mermaid.
