# The Golden Spiral -- Fibonacci Visualized

An interactive single-page web visualization that builds the Fibonacci spiral step by step, showing how simple square additions converge toward one of mathematics' most elegant constants: **phi (φ ≈ 1.6180339887...)**.

![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/Vanilla-JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

## What it does

The visualization builds the classic Fibonacci rectangle tiling and draws the golden spiral through it, one square at a time. Each step shows:

- A new square whose side length is the next Fibonacci number
- A **sum decomposition overlay** that splits the current square with a dotted line, visually proving that F(n) = F(n-1) + F(n-2) with color-coded regions, dimension brackets, and the equation displayed
- A quarter-circle **arc** connecting corners of each square, forming the continuous golden spiral
- Live-updating stats: the ratio F(n)/F(n-1) and its distance from phi, so you can watch convergence happen in real time

## Demo

Open `index.html` in any modern browser. No build step, no server, no dependencies.

## Controls

| Button | Action |
|---|---|
| **Play / Pause** | Auto-build the spiral step by step |
| **Step** | Add one Fibonacci square manually |
| **Reset** | Clear everything and start over |
| **Spiral: On/Off** | Toggle the golden spiral overlay |
| **Numbers: On/Off** | Toggle Fibonacci number labels inside squares |
| **Sum Split: On/Off** | Toggle the F(n-1) + F(n-2) decomposition on the current square |
| **Speed slider** | Control animation pace |

## Features

- **Animated spiral drawing** with a glowing tip that traces the curve as each square is added
- **Sum decomposition** on the newest square: dotted split line, blue/coral sub-regions for F(n-1) and F(n-2), dimension brackets with tick marks, and the equation rendered outside the square
- **Live convergence dashboard** showing current step, Fibonacci number, ratio, and error from phi
- **Fibonacci sequence bar** with highlighted active and current terms
- **Responsive canvas** that adapts to screen size
- Dark theme with gold accents and subtle grain texture

## How the math works

The Fibonacci sequence starts with 1, 1, and each subsequent number is the sum of the two before it:

```
1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...
```

When you divide consecutive terms, the ratio converges to the golden ratio:

```
1/1 = 1.000
2/1 = 2.000
3/2 = 1.500
5/3 = 1.667
8/5 = 1.600
13/8 = 1.625
       ...
     → 1.6180339887... = φ
```

Geometrically, placing squares with these side lengths creates a rectangle that maintains its proportions as it grows. The quarter-circle arcs through each square approximate a logarithmic spiral, the same curve found in nautilus shells, hurricane formations, and galaxy arms.

## Project structure

```
.
├── index.html    # Everything: markup, styles, and logic in a single file
└── README.md
```

The entire project is a single HTML file (~900 lines) with embedded CSS and vanilla JavaScript using the Canvas API. No frameworks, no bundlers, no external dependencies beyond two Google Fonts (Cormorant Garamond and JetBrains Mono).

## Browser support

Any modern browser with Canvas support (Chrome, Firefox, Safari, Edge).

## License

MIT -- use it however you like.
