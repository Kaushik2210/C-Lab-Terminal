# C-Lab Terminal

**An interactive study companion for MCA412-1 — Problem Solving Using C.**


**Deployed Link:https://c-lab-terminal-v-1.vercel.app/**
Every program from the lab manual, dismantled and rebuilt: syntax you can poke, code you reveal line by line, memory you watch change, and quizzes that actually score you. Built around the manual's own Smart Retail & Inventory Management domain, with a point-of-sale receipt aesthetic.

It's a single, self-contained HTML file. No build step, no dependencies, no internet required.

---

## Demo

Open `c_lab_terminal.html` in any modern browser. That's it.

```bash
# clone, then just open the file
git clone https://github.com/<your-username>/c-lab-terminal.git
cd c-lab-terminal
# macOS
open c_lab_terminal.html
# Linux
xdg-open c_lab_terminal.html
# Windows
start c_lab_terminal.html
```

To host it live on **GitHub Pages**: push to a repo, then go to **Settings → Pages → Deploy from branch → main / root**. Your app will be at `https://<your-username>.github.io/<repo-name>/c_lab_terminal.html`.

---

## Features

Each of the 8 lab programs is broken into five collapsible sections:

1. **Syntax Breakdown** — tap any element (`scanf`, `*s`, `strcmp`, `switch`, `fopen`…) to reveal what it does, *why it's used in this specific program*, and the common trap students fall into.
2. **Line-by-Line Walkthrough** — dark, syntax-highlighted code; click any highlighted line to reveal the reasoning behind it.
3. **Execution & Memory** — a live memory stepper. Step forward and back to watch variables change cell by cell (including pointer arrows and struct-to-file flow), alongside a terminal showing real input/output.
4. **Storage & The Better Version** — naive vs. expert side-by-side, with concrete rewrites (bounded `scanf`, `NULL` checks, struct padding, integer cents for money) and time/space complexity badges.
5. **Test Me** — scored quizzes: predict-the-output, spot-the-bug, and fill-in-the-blank, each with an explanation that unlocks after you answer.

Plus a global progress bar, per-program completion marking with auto-advance, and a running quiz-points counter.

---

## Programs covered

| # | Unit | Program | Concepts |
|---|------|---------|----------|
| 1 | 1 | Retail Invoice Generator | Arithmetic, relational, logical, ternary & shorthand operators |
| 2 | 1 | Inventory Valuation & Tax Calculator | Operator precedence & associativity |
| 3 | 2 | Automated Checkout System | `if-else`, `while`, `switch-case`, `break`/`continue` |
| 4 | 3 | Warehouse Aisle-Shelf Mapper | 2D arrays, nested loops, row-major traversal |
| 5 | 3 | Product Branding Validator | `strlen`, `strcpy`, `strcmp`, char arrays |
| 6 | 4 | Modular Tax & Discount Calculator | Functions, return values, pass-by-value |
| 7 | 4 | Global Stock Synchronizer | Pointers, dereferencing, call-by-reference |
| 8 | 5 | Mini Retail Ledger | Structures, file handling, `fopen`/`fprintf`/`fclose` |

---

## Tech

- Plain **HTML + CSS + vanilla JavaScript** — no frameworks, no dependencies.
- Single file (~76 KB). Fully offline. Works on desktop and mobile.
- All content and interaction logic is embedded; nothing loads from a CDN.

---

## Project structure

```
c-lab-terminal/
├── c_lab_terminal.html   # the entire app — open this
└── README.md
```

---

## Contributing

The program data lives in a `PROGRAMS` array inside the file. Each entry follows a consistent shape (`syntax`, `code`, `mem`, `output`, `better`, `quiz`), so adding a new program or quiz question is mostly a matter of copying the pattern. Pull requests that add practice-question breakdowns or fix any technical inaccuracy are welcome.

---

## Disclaimer

This is a **study aid**, not something to submit for assessment. The MCA412-1 course follows the department's AI policy for all graded work — use this to understand the material, then write your own code.

---

## License

Released under the [MIT License](LICENSE). Free to use, modify, and share.
