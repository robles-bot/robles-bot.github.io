# Daily Workflow

## Morning Routine (5-10 min)

1. **Open today's diary:** `<Leader>w<Leader>w`
2. **Set intentions:** Write 3 main goals for the day
3. **Check todo.md:** `<Leader>wt` - Review next actions
4. **Time block:** Fill in schedule section if needed

---

## Throughout the Day

### Quick Capture

Anything that comes up goes to `inbox.md` (`<Leader>wi`):

- Don't organize yet, just dump
- Format: `- [ ] [thing] :tag:` or just `- [thing]`

### Log Activities

Add timestamps to your diary:

- `<Leader>ts` inserts current time
- Keep it brief: "10:30 - Started P510 problem set"

### Work Sessions

When working on something specific:

- Open the relevant note
- Add to it as you go
- Link to other notes liberally

---

## Evening Routine (5-10 min)

1. **Process inbox:** Go through `inbox.md`
   - Move items to appropriate locations
   - Create new notes if needed
   - Delete or archive processed items

2. **Update diary:** Add reflection section
   - What went well?
   - What blocked you?
   - What's the #1 priority tomorrow?

3. **Review todo.md:** Update task statuses

---

## Weekly Review (30-60 min)

Best done on Sunday:

- [ ] **Diary review:** `<Leader>w<Leader>i` to generate index, skim the week
- [ ] **Process all inboxes:** Wiki inbox, email, physical notes
- [ ] **Update someday.md:** Add/remove items
- [ ] **Review projects:** Each active project gets a status check
- [ ] **Plan next week:** Identify top 3 priorities

---

## Student Workflow

### Course Index Structure

```markdown
# Physics 510 - Classical Mechanics

## Info
- **Professor:**
- **Schedule:** Tu/Th 5:00-6:15 PM
- **Office Hours:**
- **Textbook:**

## Links
- [Syllabus](syllabus.md)
- [Lecture Notes](lecture-notes.md)
- [Problem Sets](problem-sets.md)
- [Exam Prep](exam-prep.md)

## Progress
| Week | Topic | HW | Status |
|------|-------|-----|--------|
| 1 | Newtonian mechanics | PS1 | Done |
| 2 | Lagrangian | PS2 | In Progress |

## Key Concepts
- [[research/concepts/lagrangian-mechanics]]
- [[research/concepts/hamiltonian-mechanics]]

---
:course: :physics:
```

### Lecture Notes Strategy

**During lecture:**

- Focus on understanding, not transcription
- Write key points, questions, diagrams
- Mark unclear parts with `???`

**After lecture (within 24 hrs):**

- Review and expand notes
- Link to concept notes in research/
- Add to problem set or exam prep as relevant

### Problem Set Flow

1. **Start:** Create problem set note from template
2. **Attempt:** Work each problem, document approach
3. **Stuck?** Mark and move on, return later
4. **Verify:** Check against solution, note errors
6. **Reflect:** What concepts need more review?
