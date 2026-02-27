# Research Workflow

A Zettelkasten-inspired system for theoretical and computational research.

---

## Capturing Research Ideas

When an idea strikes, dump it in `inbox.md`:

```markdown
# inbox.md
- [ ] Idea: What if we apply Monte Carlo to the XY model with disorder? :research: :idea:
- [ ] Question: How does DFT handle strongly correlated systems? :research: :question:
- [ ] Follow up: Re-read Anderson localization paper :literature:
```

---

## Processing into Zettelkasten

After processing, create atomic notes:

```markdown
# research/concepts/anderson-localization.md

# Anderson Localization

## Definition
The absence of diffusion of waves in a disordered medium.

## Key Physics
In a sufficiently disordered system, quantum interference effects cause
wavefunctions to become exponentially localized...

## Mathematical Framework
$$\psi(r) \sim e^{-|r-r_0|/\xi}$$
where $\xi$ is the localization length.

## Computational Approaches
- Exact diagonalization for small systems
- Transfer matrix method for quasi-1D
- Kernel polynomial method for large systems

## Related Concepts
- [[metal-insulator-transition]]
- [[weak-localization]]
- [[random-matrix-theory]]

## Key Papers
- [[research/literature/anderson1958-absence-diffusion]]
- [[research/literature/abrahams1979-scaling-theory]]

---
:concept: :condensed-matter: :disorder:
```

---

## Literature Management

When reading a paper:

1. Create note: `research/literature/[author][year]-[short-title].md`
2. Fill in template as you read
3. Link to relevant concept notes
4. Add to `research/inbox.md`: follow-up papers to read

---

## Computational Research Notes

Example structure for `research/methods/molecular-dynamics.md`:

> **# Molecular Dynamics**
>
> **Overview:** Classical simulation of particle motion using Newton's equations.
>
> **Algorithm:**
>
> 1. Initialize positions and velocities
> 2. Calculate forces from potential
> 3. Integrate equations of motion
> 4. Repeat

**Code Snippet (Python/ASE):**

```python
from ase import Atoms
from ase.md.velocitydistribution import MaxwellBoltzmannDistribution
from ase.md.verlet import VelocityVerlet

# Setup
atoms = ...
MaxwellBoltzmannDistribution(atoms, temperature_K=300)

# Run
dyn = VelocityVerlet(atoms, timestep=1.0 * units.fs)
dyn.run(steps=1000)
```

**Common Pitfalls:**

- Time step too large → energy drift
- Poor thermostat choice → incorrect ensemble
- Finite size effects

**Packages:** ASE, LAMMPS, GROMACS

**Related concepts:** verlet-integration, thermostats, periodic-boundary-conditions

**Tags:** `:method: :simulation: :computational:`

---

## Thesis Progress Tracking

Create `school/thesis/progress.md` with this structure:

| Section | Content |
|---------|---------|
| **Working Title** | Your thesis title |
| **Committee** | Advisor + members |
| **Timeline** | Milestones table (lit review, proposal, defense, etc.) |
| **Chapters** | Checklist of chapters |
| **Current Focus** | What you're working on this week |
| **Open Questions** | Research questions to resolve |
| **Meeting Log** | Date, discussed, action items |

**Example Timeline Table:**

| Milestone | Target | Status |
|-----------|--------|--------|
| Literature review | | |
| Proposal | | |
| First results | | |
| Draft to advisor | | |
| Defense | | |

**Tags:** `:thesis:`
