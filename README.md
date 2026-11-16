# Reward hacking in a block-stacking world

A book club reflection on Bruce Schneier's *A Hacker's Mind* (AIPI 590.01). A toy block-stacking world where a tabular Q-learning agent learns to hack three different reward rules.

Everything lives in one file, `index.html`, written in plain HTML, CSS and JavaScript. There are no frameworks and no network calls apart from the optional Google Fonts.

## Run it

Open `index.html` in a browser.

## Host it on GitHub Pages

1. Push this repository to GitHub.
2. In the repository settings, open Pages and choose the `main` branch, root folder.
3. The empty `.nojekyll` file tells Pages to serve the file as it is.

## What the demo does

- Trains a Q-learning agent (20,000 episodes of 12 steps, gamma 0.95, alpha decaying from 0.3 to 0.01, epsilon from 0.3 to 0.02, seeded with mulberry32).
- Runs 2,000 greedy test episodes and reports how many end with block B upright on block A.
- Lets you watch one greedy run step by step.

Typical results with the fixed seed (about 80% means 78 to 82% across seeds):

| Reward | Ledge | Upright on A |
| --- | --- | --- |
| Bottom-face height | no or yes | 0% |
| Raised and upright | no | about 80% |
| Raised and upright | yes | 0% |
| On A and upright | no or yes | about 80% |

## Before you publish

Fill in the two `[YOUR WORDS HERE]` boxes near the end of the page, and edit the "What I take from it" section so it says what you think.

The simulation code sits between the `SIM:START` and `SIM:END` comments, with no DOM references, so it can be loaded in Node for testing.
