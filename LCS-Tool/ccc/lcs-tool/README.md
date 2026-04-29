# ⟨/⟩ LCS Tool — Longest Common Subsequence Analyzer

> A visually stunning, browser-based tool to compare two texts using the **Longest Common Subsequence** dynamic programming algorithm — featuring a live DP matrix, similarity scoring, and plagiarism-style highlighting.

![LCS Tool](https://img.shields.io/badge/Algorithm-Dynamic%20Programming-7c6bff?style=for-the-badge)
![Vanilla](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JS-00d4ff?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-22d3a0?style=for-the-badge)

---

## 📸 Features

| Feature | Description |
|---|---|
| 🔤 **Dual Text Editor** | Paste text, type, or upload `.txt` files for both inputs |
| 🔡 **Char / Word Mode** | Toggle between character-level and word-level comparison |
| 🔠 **Case Sensitivity** | Optional case-sensitive matching |
| 📊 **Similarity Score** | Percentage score with animated color-coded meter |
| 🟣 **LCS Highlighting** | Matched tokens highlighted in both texts side-by-side |
| 🔢 **DP Matrix Viewer** | Full `(m+1)×(n+1)` table with path, match cells & arrows |
| ▶ **Matrix Animation** | Watch the DP table fill cell-by-cell in real time |
| 📚 **About / Learn** | Algorithm explanation + complexity comparison table |

---

## 🚀 Getting Started

No build tools or server required. Just open the file in any modern browser.

```bash
# Clone or download the project
git clone https://github.com/your-username/lcs-tool.git
cd lcs-tool

# Open directly in browser
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

Or simply **double-click** `index.html`.

---

## 📁 Project Structure

```
lcs-tool/
├── index.html   # Main HTML — three-tab layout (Compare, DP Matrix, About)
├── style.css    # Dark glassmorphism design system + animations
├── app.js       # LCS algorithm, DP traceback, matrix renderer, UI logic
└── README.md    # This file
```

---

## 🧠 Algorithm

### Recurrence Relation

```
If A[i] == B[j]:
    dp[i][j] = dp[i-1][j-1] + 1       // diagonal — match

Else:
    dp[i][j] = max(dp[i-1][j],         // from above
                   dp[i][j-1])          // from left
```

### Traceback

Starting at `dp[m][n]`, walk backwards:
- **↖ Diagonal** → character match, add to LCS
- **↑ Up** → skip character from A
- **← Left** → skip character from B

### Complexity

| Metric | Value |
|---|---|
| Time | O(m × n) |
| Space | O(m × n) |
| Similarity formula | `LCS_len / max(len_A, len_B) × 100%` |

---

## 🎨 Design

- **Theme**: Dark glassmorphism — `#090c14` base
- **Accent colors**: Purple `#7c6bff` + Cyan `#00d4ff`
- **Fonts**: Inter (UI) + JetBrains Mono (code/tokens)
- **Animations**: Floating particles, meter fill, token pop-in, matrix reveal
- **Responsive**: Works on mobile, tablet, and desktop

---

## 📝 Usage Tips

- Use **Word mode** for longer texts (articles, essays) — much faster and more meaningful
- Use **Char mode** for short strings, DNA sequences, or precise character-level analysis
- The **DP Matrix** is capped at 30×30 for display, but the full matrix is always computed
- Upload `.txt` files directly using the **📄 Load file** buttons

---

## 📜 License

MIT — free to use, modify, and distribute.
