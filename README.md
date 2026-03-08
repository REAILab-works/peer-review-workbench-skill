# Peer Review Workbench

A standalone Codex skill for journal-style manuscript peer review.

## What it does

- outputs `Reject`, `Major Revision`, `Minor Revision`, or `Accept`
- drafts a confidential note to editor
- drafts major comments for authors
- drafts minor comments for authors
- produces a prioritized revision checklist

## Files

```text
SKILL.md
agents/openai.yaml
```

## Recommended prompt

```text
Use $peer-review-workbench to review my manuscript for [Journal Name]. The file is [/absolute/path/to/manuscript.docx]. Please provide a recommendation, confidential note to editor, major comments, minor comments, and a prioritized revision list.
```
