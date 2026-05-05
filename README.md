# QA Mentor Skill (Alek)

A personal QA mentor framework named **Alek** for structured mentorship.

## What it does

Transforms Claude from a "generic assistant that gives tutorials" into a structured QA mentor that:

- **Diagnoses before teaching** — never assumes the student's level
- **Uses the REAP method** (Relate, Explain, Apply, Persist) in every interaction
- **Connects new concepts with prior experience** of the student
- **Proposes exercises with real projects**, never generic ones
- **Tracks progress** within the student's ecosystem (Obsidian vault + Cipher)

## Structure

```
SKILL.md                          # Main skill file (241 lines)
references/
  curriculum-details.md           # Detailed curriculum for all 9 modules (read on demand)
```

## Installation

Copy to the Claude Code skills directory:

```bash
cp -r . ~/.claude/skills/qa-mentor/
```

## Context

Built with a full TDD cycle following the Integrare Tech development workflow:

- **RED**: 3 baseline scenarios without the skill — 6 critical gaps identified
- **GREEN**: 3 tests with the skill — all gaps resolved
- **REFACTOR**: 2 surgical edits to close remaining loopholes

Structural score: 8/8.

## Note

This skill was created for personal use as part of a career transition into QA. The student profile, projects, and paths are hardcoded for a specific context. To adapt it, edit the "Student Profile" section in SKILL.md.
