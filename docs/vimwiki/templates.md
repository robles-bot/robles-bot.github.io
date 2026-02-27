# Templates

These templates auto-insert when creating new files in specific directories (see [Setup](setup.md) for the autocmd configuration).

---

## Diary Template

**Location:** `templates/diary.md`
**Triggers on:** `~/vimwiki/diary/YYYY-MM-DD.md`

```markdown
# {{DATE}}

## Intentions
*What do I want to accomplish today?*

- [ ]
- [ ]
- [ ]

## Schedule
| Time | Activity |
|------|----------|
| 09:00 | |
| 12:00 | |
| 15:00 | |

## Log
*Record what actually happened*


## Capture
*Quick thoughts, ideas, links to process later*


## Reflection
*End of day: What went well? What could improve?*


---
:diary:
```

---

## Lecture Template

**Location:** `templates/lecture.md`
**Triggers on:** `~/vimwiki/school/*/lecture-*.md`

```markdown
# Lecture: [TOPIC]
**Course:** [COURSE]
**Date:**
**Professor:**

## Key Concepts


## Notes


## Questions
- [ ]


## Connections
*Links to other concepts:*
- [[]]

## Action Items
- [ ] Review by:
- [ ] Problem set:

---
:lecture: :physics:
```

---

## Research Concept Template

**Location:** `templates/concept.md`
**Triggers on:** `~/vimwiki/research/concepts/*.md`

```markdown
# [CONCEPT NAME]

## Definition
*One sentence explanation*


## Detailed Explanation


## Mathematical Formulation
$$

$$

## Computational Implementation
```python

```

## Key Papers
- [[research/literature/]]

## Related Concepts
- [[]]
- [[]]

## Applications


## Open Questions
-

---
:concept: :research:
```

---

## Paper Review Template

**Location:** `templates/paper-review.md`
**Triggers on:** `~/vimwiki/research/literature/*.md`

```markdown
# [Author et al. (Year)] - [Short Title]

## Metadata
- **Title:**
- **Authors:**
- **Journal:**
- **Year:**
- **DOI/arXiv:**
- **Date Read:**

## Summary
*2-3 sentences: What is this paper about?*


## Key Contributions
1.
2.
3.

## Methods


## Key Results


## Relevance to My Research
*How does this connect to my work?*


## Critical Notes
*Limitations, questions, disagreements*


## Key Equations/Figures
*Copy or reference the most important ones*


## Citations to Follow
- [ ]

## Quotes
> "..."

---
:literature: :physics:
```

---

## Problem Set Template

**Location:** `templates/problem-set.md`

```markdown
# Problem Set [#]
**Course:**
**Due:**
**Status:** [ ] Not Started / [ ] In Progress / [x] Complete

## Problems

### Problem 1
**Topic:**

**Given:**


**Solution:**


**Verified:** [ ] Analytically / [ ] Numerically / [ ] With classmate

---

### Problem 2
...

## Reflection
*What concepts did this reinforce? What's still unclear?*


---
:homework: :physics:
```

---

## Project Template

**Location:** `templates/project.md`

```markdown
# Project: [NAME]

## Overview
*One paragraph description*


## Goals
- [ ]
- [ ]

## Status
**Current Phase:** Planning / Active / Review / Complete
**Last Updated:**

## Tasks
### Active
- [ ]

### Completed
- [x]

## Notes


## Resources
-

## Log
### [DATE]


---
:project:
```

---

## Meeting Template

**Location:** `templates/meeting.md`

```markdown
# Meeting: [TOPIC]
**Date:**
**Attendees:**
**Location:**

## Agenda
1.
2.

## Notes


## Action Items
- [ ] @me:
- [ ] @them:

## Next Meeting


---
:meeting:
```
