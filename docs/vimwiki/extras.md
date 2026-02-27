# Extras

Additional workflows for code notes, reading, and hobbies.

---

## Code & Developer Notes

### Snippet Library

Organize snippets by language in `code/snippets/`. Example structure for `python.md`:

**File I/O - Read CSV:**

```python
import pandas as pd
df = pd.read_csv('file.csv')
```

**File I/O - Read JSON:**

```python
import json
with open('file.json') as f:
    data = json.load(f)
```

**NumPy - Create array:**

```python
import numpy as np
arr = np.linspace(0, 10, 100)
```

**Matplotlib - Basic plot:**

```python
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plt.plot(x, y)
plt.xlabel('x')
plt.ylabel('y')
plt.savefig('plot.pdf')
```

**Tags:** `:snippet: :python:`

---

### Tool Documentation

Example for `code/tools/hpc-clusters.md`:

**NERSC (Perlmutter) - Login:**

```bash
ssh username@perlmutter.nersc.gov
```

**Job Submission:**

```bash
sbatch job.slurm
squeue -u $USER
scancel JOBID
```

**Sample SLURM Script:**

```bash
#!/bin/bash
#SBATCH -A m1234
#SBATCH -C cpu
#SBATCH -q regular
#SBATCH -t 01:00:00
#SBATCH -N 1

srun python my_script.py
```

**Tags:** `:hpc: :tools:`

---

## Reading & Literature

### Reading Dashboard

Structure for `reading/index.md`:

```markdown
# Reading

## Currently Reading
| Book | Progress | Notes |
|------|----------|-------|
| [[notes/meditations]] | Ch. 3 | |

## Quick Links
- [To Read List](to-read.md)
- [Completed](completed.md)
- [Book Notes](notes/)

## Reading Goals
- [ ] 12 books in 2026
- [ ] 1 philosophy book per quarter

## Stats
- 2026: 0/12 completed
```

### Book Notes Structure

Structure for `reading/notes/[book-name].md`:

```markdown
# Meditations - Marcus Aurelius

## Metadata
- **Author:** Marcus Aurelius
- **Started:**
- **Finished:**
- **Rating:** /5

## Summary

## Key Ideas
1.
2.
3.

## Favorite Quotes
> "Quote here" (Book X, Section Y)

## How It Applies to My Life

## Related
- [[reading/notes/letters-from-a-stoic]]

---
:book: :philosophy: :stoicism:
```

