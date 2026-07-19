# ML Bootcamp Progress

## Day 0 — Environment Setup
- [x] Python 3.12.7 + virtual environment
- [x] VS Code configured with Python, Jupyter, Pylance extensions
- [x] Core ML libraries installed (numpy, pandas, matplotlib, seaborn, scikit-learn, jupyter)
- [x] Git configured (name, email, version 2.50.1)
- [x] Project folder structure created
- [x] GitHub repo connected and pushed
- [x] Google Colab familiarized (GPU runtime, Drive mount, !pip)
- [x] Kaggle account + API set up

Hardest bug today: Two Pythons on the same machine fighting over PATH
Concept I still don't fully get: ___

## Day 1 — Coming up
- Python for ML (the parts that actually matter)
- List/dict comprehensions, functions, slicing, OOP basics

## Week 1 — Python & Data Foundations

### Day 1 — Python for ML ✅
Topics covered:
- List, dict, and set comprehensions (including the duplicate-key gotcha in dict comprehensions — last write wins silently)
- `enumerate` and `zip` (including `zip`'s silent truncation to the shorter iterable)
- f-strings and format specs (`.4f`, `.2e`, `,` for thousands, `>15` for right-alignment)
- `*args` and `**kwargs` — collect in a `def`, unpack in a call, and the forwarding relay pattern
- Lambdas — inline anonymous functions for `key=` in `sorted`/`max`/`min`, and when *not* to reach for them
- Exception handling — specific exceptions with `as e`, the `try` / `except` / `else` / `finally` structure, and why bare `except` is a silent-failure trap
- `if __name__ == "__main__":` — definitions above, actions inside; makes a file both an importable module and a runnable script
- Light OOP — classes, `__init__`, `self`, `super().__init__()`; enough to read a PyTorch model class

Design work:
- `summary_stats(records)` — went from vague spec through 5 design decisions to a working, tested implementation. First reps of "think before you type."

Reading practice:
- Confirmed I can spot today's Python patterns in real Kaggle notebooks (lambdas in `.apply()`, comprehensions filtering columns, `enumerate` over `kf.split()` pairs, `super().__init__()` in a `Dataset` subclass, `try` / `except ValueError`).

Watching for (not fuzzy today, but flagged):
- `*args` / `**kwargs` collect-vs-unpack symmetry in unfamiliar framework code — revisit today's relay example if it feels shaky in context.

Mini-projects done: 0/10
Medium projects done: 0/3

---

### Day 2 — NumPy (part 1)
- [ ] Not started