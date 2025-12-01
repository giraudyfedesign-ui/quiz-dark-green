# JavaScript Quiz App

An interactive quiz application testing JavaScript fundamentals with timed questions, instant feedback, and detailed results.

![Quiz App Preview](https://img.shields.io/badge/Status-Live-brightgreen) ![HTML](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## Overview

A fully functional quiz app featuring 10 JavaScript questions covering fundamentals, ES6+ syntax, and common patterns. Includes a countdown timer, progress tracking, instant answer feedback with explanations, and a comprehensive results screen.

## Features

- **Start Screen** — Quiz overview with stats (questions, time, difficulty)
- **Progress Bar** — Visual progress and running score
- **Timed Questions** — 30-second countdown per question
- **Code Snippets** — Syntax-highlighted code examples
- **Instant Feedback** — Correct/incorrect highlighting
- **Explanations** — Educational notes after each answer
- **Results Screen** — Final score, stats, performance message
- **Retry Option** — Play again without page refresh
- **Responsive** — Works on mobile and desktop

## Quiz Topics

The 10 questions cover:
- `typeof` operator quirks
- Array methods (`map`, `filter`, `reduce`)
- Reference vs. value types
- Equality operators (`==` vs `===`)
- Spread operator
- Closures
- Type coercion
- `let` vs `const`
- Async/await
- Method chaining

## Tech Stack

- HTML5
- CSS3 (Custom properties, Animations)
- Vanilla JavaScript (ES6+)
- Google Fonts (Instrument Serif, DM Sans)

## Skills Demonstrated

- **State Management** — Tracking question index, score, answers
- **DOM Manipulation** — Dynamic content rendering
- **Timer Functions** — `setInterval` for countdown
- **Event Handling** — Click events, keyboard navigation
- **Conditional Logic** — Answer validation, score calculation
- **CSS Animations** — Fade transitions, progress bar
- **UI Feedback** — Loading states, success/error styling

## How It Works

### Quiz Flow
```
Start Screen → Questions (1-10) → Results Screen
                    ↓
              Select Answer
                    ↓
              Show Feedback
                    ↓
              Next Question
```

### Scoring
- Each correct answer = 1 point
- Final score = (correct / total) × 100%
- Performance tiers:
  - 80%+ = "Excellent!"
  - 50-79% = "Good Job!"
  - Below 50% = "Keep Learning!"

### Timer
- 30 seconds per question
- Visual warning at 10 seconds (yellow)
- Critical warning at 5 seconds (red)
- Auto-submits wrong answer if time expires

## Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/yourusername.github.io.git
   ```

2. Open `quiz-app.html` in your browser

## Customization

### Adding Questions

Edit the `questions` array in the JavaScript:

```javascript
{
    question: "Your question text here",
    code: `optional code snippet`, // or omit for no code
    answers: [
        { text: "Option A", correct: false },
        { text: "Option B", correct: true },
        { text: "Option C", correct: false },
        { text: "Option D", correct: false }
    ],
    explanation: "Explanation shown after answering"
}
```

### Adjusting Timer

Change the `timeLeft` value in `startTimer()`:

```javascript
timeLeft = 30; // seconds per question
```

## File Structure

```
quiz-app.html
├── <style>              # All CSS (embedded)
├── <body>
│   ├── .quiz-header     # Title and branding
│   ├── .progress        # Progress bar
│   ├── .quiz-card
│   │   ├── #startScreen    # Welcome screen
│   │   ├── #questionScreen # Question UI
│   │   └── #resultsScreen  # Final results
└── <script>
    ├── questions[]      # Quiz data
    ├── State variables  # Score, index, timer
    ├── DOM references   # Element selectors
    └── Functions        # Quiz logic
```

## Future Enhancements

Potential improvements:
- [ ] Question randomization
- [ ] Difficulty levels
- [ ] Category selection
- [ ] Local storage for high scores
- [ ] Share results feature

## License

MIT License
