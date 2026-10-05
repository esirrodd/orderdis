---
name: notes-rework
description: Follow a note as the user reworks it, carrying out the instructions he writes into it and keeping the note coherent and cleanly formatted.
disable-model-invocation: true
argument-hint: "\"노트.md\""
---

## In this session

The user reworks the note "$0" over many turns to match his own priorities and intent — thinking the subject through, or deliberating on what the subject should even be, or on what that intent even is.

Claude follows along:
- When he says something like "바꿨어" or "고쳤어", check what changed.
- If the intent behind a change isn't apparent, flag it and have him clarify before editing.

## In the note

HTML comments are the user's messages to Claude. He puts them in the note rather than in chat when the message belongs to a particular spot. For example:
- work instruction: `<!-- 이 아이디어는 폐기됐으니, 삭제하고, 관련 내용 정리해 -->`
- question: `<!-- 이거 다른 방법으로 구현 가능할까? -->`
- caveat: `<!-- 이 헤더의 내용은 확정이 아니야 -->`

Keep the note lean:
- Delete whatever no longer fits the note's shifted subject or his intent. Don't add anything about what changed or why.
- Answer his HTML-comment questions in chat.

Complete rough links into proper markdown:
- external resource: `참고: [label](url)`
- another note under `~/세계/`: `[본문에서 이어지는 설명](<예시 폴더/예시 노트.md#헤더 제목>)` — path relative to `~/세계/`; `#헤더 제목` optional.

Also:
- Use Mermaid when a structural diagram is needed.
- Delete each HTML comment once it's resolved.
- Clean up non-standard markdown.

Finally, fix any inconsistencies the preceding changes introduced.