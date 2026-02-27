# GTD System

Implementation of David Allen's Getting Things Done methodology in Vimwiki.

---

## Inbox (`inbox.md`)

Everything starts here. Don't organize, just capture:

```markdown
# Inbox

## Capture
- Email professor about thesis meeting
- Look into NERSC allocation application
- Buy groceries
- Interesting paper on arxiv: 2402.xxxxx
- Fix bike tire

## Processing Queue
*Items being sorted:*
```

---

## Next Actions (`todo.md`)

Only actionable items with clear next steps:

```markdown
# Next Actions

## High Priority (Do Today)
- [ ] Complete P510 Problem Set 3 - due tomorrow
- [ ] Email advisor: schedule thesis meeting

## School :school:
- [ ] Review Lagrangian notes before Thursday
- [ ] Start P522 reading: Chapter 4

## Research :research:
- [ ] Run simulation with new parameters
- [ ] Read Smith et al. paper

## Code :code:
- [ ] Fix bug in analysis script
- [ ] Update GitHub page

## Life :life:
- [ ] Buy groceries
- [ ] Fix bike tire

## Waiting For
- [ ] @Advisor: feedback on draft
- [ ] @Amazon: textbook delivery

---
*Last reviewed: [DATE]*
```

---

## Someday/Maybe (`someday.md`)

Ideas and projects not active now:

```markdown
# Someday/Maybe

## Research Ideas
- Explore machine learning for phase classification
- Learn Julia for scientific computing

## Courses to Take
- Physics 562 - Advanced Computational Methods
- Audit a math course on group theory

## Books to Read
- Landau & Lifshitz complete series
- Being and Nothingness

## Projects
- Build personal website with research portfolio
- Create physics visualization YouTube channel

## Life
- Learn to cook 10 new recipes
- Visit national parks

---
*Review monthly*
```

---

## Projects List

Each active project gets its own note. Track them in one place:

```markdown
# Active Projects

| Project | Location | Next Action | Status |
|---------|----------|-------------|--------|
| Thesis | school/thesis/ | Literature review | Active |
| PYAR Notebooks | code/projects/pyar | Fix Notebook 4 | Active |
| GitHub Page | code/projects/github-page | Add publications | Paused |

*Archived projects: [[archive/]]*
```

---

## The GTD Flow

```
┌─────────────┐
│   CAPTURE   │  Everything goes to inbox.md
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   CLARIFY   │  Is it actionable?
└──────┬──────┘
       │
   ┌───┴───┐
   │       │
   ▼       ▼
  YES      NO → Reference, Someday, or Trash
   │
   ▼
┌─────────────┐
│  ORGANIZE   │  Next action? Project? Waiting?
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   REFLECT   │  Weekly review
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   ENGAGE    │  Do the work
└─────────────┘
```

---

## Weekly Review Checklist

- [ ] **Get Clear**
    - [ ] Process inbox.md to zero
    - [ ] Process email inbox
    - [ ] Process physical notes/papers
    - [ ] Review diary entries from past week

- [ ] **Get Current**
    - [ ] Review todo.md - update statuses
    - [ ] Review each active project
    - [ ] Review waiting-for items
    - [ ] Review someday/maybe list

- [ ] **Get Creative**
    - [ ] What new projects/ideas emerged?
    - [ ] What's the #1 priority for next week?
    - [ ] Any blocked items to unblock?
