# LaTeX Snippets (UltiSnips)

These snippets work in vimwiki files via `~/.vim/UltiSnips/vimwiki.snippets`.

!!! note "Trigger Key Configuration"
    By default, UltiSnips uses `<Tab>` to expand snippets. However, this can conflict with other plugins (like autocompletion). I use `<C-l>` instead.

    To change your trigger key, add to your `.vimrc`:

    ```vim
    " Change snippet expansion trigger (default is <Tab>)
    let g:UltiSnipsExpandTrigger="<C-l>"
    let g:UltiSnipsJumpForwardTrigger="<C-l>"
    let g:UltiSnipsJumpBackwardTrigger="<C-h>"
    ```

    Throughout this guide, when you see `<Tab>`, substitute your configured trigger key.

## Snippet Inheritance Chain

```
vimwiki.snippets
    ├── extends math.snippets      (Greek letters, frac, brackets)
    ├── extends physics.snippets   (dots, vectors, bra-ket, ∂, etc.)
    └── extends texmath.snippets   (integrals, ∇ operators, sums)

markdown.snippets
    └── extends vimwiki.snippets   (all of the above)
```

---

## Greek Letters

| Trigger | Output | Trigger | Output |
|---------|--------|---------|--------|
| `;a` | `\alpha` | `;A` | - |
| `;b` | `\beta` | `;B` | - |
| `;g` | `\gamma` | `;G` | `\Gamma` |
| `;d` | `\delta` | `;D` | `\Delta` |
| `;e` | `\epsilon` | `;ve` | `\varepsilon` |
| `;th` | `\theta` | `;Th` | `\Theta` |
| `;l` | `\lambda` | `;L` | `\Lambda` |
| `;m` | `\mu` | `;n` | `\nu` |
| `;p` | `\pi` | `;P` | `\Pi` |
| `;r` | `\rho` | `;s` | `\sigma` |
| `;t` | `\tau` | `;ph` | `\phi` |
| `;ps` | `\psi` | `;Ps` | `\Psi` |
| `;w` | `\omega` | `;W` | `\Omega` |
| `;x` | `\xi` | `;X` | `\Xi` |
| `;ch` | `\chi` | `;S` | `\Sigma` |

---

## Math Structures

| Trigger | Output | Description |
|---------|--------|-------------|
| `frac` | `\frac{a}{b}` | Fraction |
| `p` | `\left( \right)` | Parentheses |
| `b` | `\left[ \right]` | Brackets |
| `c` | `\left\{ \right\}` | Braces |
| `sum` | `\sum_{i}^{n}` | Summation |
| `prod` | `\prod_{i}^{n}` | Product |
| `int` | `\int_{a}^{b} f(x)\,dx` | Integral |
| `iint` | `\iint_{D}` | Double integral |
| `oint` | `\oint_{C}` | Contour integral |

---

## Physics

| Trigger | Output | Description |
|---------|--------|-------------|
| `dot` | `\dot{x}` | Time derivative |
| `ddot` | `\ddot{x}` | Second time derivative |
| `vva` | `\vec{v}` | Vector (arrow) |
| `vvb` | `\bm{v}` | Vector (bold) |
| `uhat` | `\hat{n}` | Unit vector |
| `bra` | `\bra{\psi}` | Dirac bra |
| `ket` | `\ket{\psi}` | Dirac ket |
| `braket` | `\braket{\phi}{\psi}` | Bracket |
| `expv` | `\langle O \rangle` | Expectation value |
| `lag` | `\mathcal{L}` | Lagrangian |
| `ham` | `\mathcal{H}` | Hamiltonian |
| `pd` | `\partial` | Partial symbol |
| `pdd` | `\frac{\partial f}{\partial q}` | Partial derivative |
| `grad` | `\nabla f` | Gradient |
| `div` | `\nabla \cdot \bm{F}` | Divergence |
| `curl` | `\nabla \times \bm{F}` | Curl |
| `lap` | `\nabla^2 f` | Laplacian |

---

## Vimwiki-Specific

| Trigger | Output | Description |
|---------|--------|-------------|
| `dm` | `$$ ... $$` | Display math block |
| `ali` | Aligned equations | Multi-line aligned |
| `cas` | Cases environment | Piecewise functions |
| `eql` | **Eq. name:** `$$ $$` | Labeled equation |
| `prob` | Full problem template | Given/Find/Solution/Answer |
| `EL` | Euler-Lagrange equation | Full equation |
| `schro` | Schrödinger equation | Full equation |
| `newton` | Newton's 2nd law | `\sum F = ma` |
| `[[` | `[[link]]` | Wiki link |
| `ref` | `[[research/literature/]]` | Literature link |
| `con` | `[[research/concepts/]]` | Concept link |

---

## Example Usage

Type this in a vimwiki file:

```
dm<Tab>
lag<Tab> = frac<Tab>1<Tab>2<Tab>m dot<Tab>q<Tab>^2 - V(q)
```

Expands to:

$$
\mathcal{L} = \frac{1}{2}m \dot{q}^2 - V(q)
$$
