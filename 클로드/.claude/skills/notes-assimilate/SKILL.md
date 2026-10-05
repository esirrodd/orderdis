---
name: notes-assimilate
description: Follow a note as the user assimilates it, verifying each round of his edits and keeping the note consistent.
disable-model-invocation: true
argument-hint: "\"노트.md\""
---

## This session

- The user is assimilating the note "$0" — perusing and revising it himself over many turns until it matches his own understanding and priorities.
- Claude follows the note's direction: what he has changed, and what he is changing it toward. When he says something like "바꿨어" or "고쳤어", work in this order: check first, then edit, then the final sweep.

## Check

- Catch what is wrong, not what is missing — changes that are mistaken or inconsistent, not ones that merely reflect priorities of his own. 
- Reality-check the generalizations and examples he added: do they carry real weight for learning, or are they trivial or true only in a narrow case?
- Watch for latent misunderstandings — changes that read fine sentence by sentence but rest on a mistaken premise.

If the intent behind a change isn't apparent, flag it and have him clarify before editing.

## Edit

HTML-comments are the user's messages to Claude. He leaves them in the note rather than in chat when a message belongs to a particular spot. For example:
- work instruction: `<!-- 위 표를 아래 구조도에 녹여줘 -->`
- question: `<!-- 이 단락, 이 위치에 넣은 이유가 있어? -->`
- caveat: `<!-- 이 아래부터는 아직 안읽었어, 그리고 내가 잘 모르는 내용이야 -->`

Rough links he left incomplete; finish them as proper markdown links:
- external resource: `참고: [label](url)`
- another note under `~/세계/`: `[본문에서 이어지는 설명](<예시 폴더/예시 노트.md>)` — absolute path with `~/세계/` stripped off.

Tidying and formatting:
- Any header may carry a line starting with `>` directly beneath it: under the H1, an overview of the note and why it matters; under any other header, a supplement for when the header alone doesn't say enough. Revise these as needed.
- Use Mermaid when a structural diagram is needed.
- Delete HTML comment markers once they're resolved.
- Clean up non-standard markdown anywhere in the note.

Finally, sweep the whole note: fix any inconsistency the preceding changes introduced, and settle the formatting left over from the pass above.
