Password-Strength-Analyzer
A simple tool that tells you how strong your password actually is
Live demo: https://thanmay198.github.io/Password-Analyzer/
This is a small, single-page tool for checking password strength. Instead of
just ticking boxes like "has a number" or "has a symbol," it measures actual
randomness (entropy) and turns that into a score you can read at a glance.
No frameworks, no build tools, no backend — just one HTML file.
What it does
Watches as you type — there's no submit button. Type a password and the
results update instantly.
Calculates real entropy — figures out which character types you've
used (lowercase, uppercase, numbers, symbols) and works out how many bits
of randomness your password actually represents.
Scores it out of 100 — entropy is capped at 100 so the number stays
easy to compare across different passwords.
Gives a plain verdict — Very Weak, Weak, Fair, Strong, or Very Strong,
based on where the score lands.
Doesn't store anything — the password you type never leaves the
browser tab. Nothing is saved, sent, or logged anywhere.
Files in this repo
```
├── index.html     # the tool itself — markup, styling, and logic all in one file
└── README.md      # this file
```
How the scoring works
Step	What happens
Pool size	Adds up which character types are present — 26 for lowercase, 26 for uppercase, 10 for digits, 32 for symbols
Entropy	`password length × log2(pool size)` — the standard way to estimate randomness in bits
Score	Entropy rounded and capped at 100
Verdict	Under 20 = Very Weak, under 40 = Weak, under 60 = Fair, under 80 = Strong, 80+ = Very Strong
Trying it out
Just open `index.html` in a browser — that's it. No installation, no
dependencies, nothing to configure.
