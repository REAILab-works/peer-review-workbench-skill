# Peer Review Workbench

A standalone Codex skill for journal-style manuscript peer review.

中英双语的论文审稿技能，用于把完整稿件转成结构化审稿意见，而不是作者侧修稿建议。

It is designed for users who want Codex to act like a reviewer, not an author-side reviser.

This bilingual skill is designed to turn a full manuscript into a structured reviewer report, not into author-side revision text.

## What it does

- outputs `Reject`, `Major Revision`, `Minor Revision`, or `Accept`
- drafts a confidential note to editor
- drafts major comments for authors
- drafts minor comments for authors
- produces a prioritized revision checklist

## Best use cases

- draft a first-round reviewer report
- simulate a second-round or revision-round review
- pressure-test a manuscript before journal submission
- turn a full manuscript into structured reviewer comments

## Repository structure

```text
SKILL.md
agents/openai.yaml
examples/
```

## Recommended prompt

```text
Use $peer-review-workbench to review my manuscript for [Journal Name]. The file is [/absolute/path/to/manuscript.docx]. Please provide a recommendation, confidential note to editor, major comments, minor comments, and a prioritized revision list.
```

## Example prompts

See:

- `examples/first_round_review.txt`
- `examples/revision_round_review.txt`
- `examples/editor_screening.txt`

## Notes

- This skill assumes the manuscript file is available.
- It is optimized for structured peer-review output rather than direct manuscript rewriting.
- It should not be used to fabricate line-by-line comments for a paper that has not been provided.

## License

MIT
