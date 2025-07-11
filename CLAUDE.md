# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

jsdate.wtf is a single-page web application that presents an interactive quiz about JavaScript's Date object quirks and unexpected behaviors. The entire application is contained in a single `index.html` file with no external dependencies or build process required.

## Development Commands

This is a static HTML file with no build process. To develop locally:

```bash
# Option 1: Open directly in browser
open index.html

# Option 2: Serve with Python
python -m http.server 8000

# Option 3: Serve with Node.js
npx serve

# Option 4: Use any static file server
```

## Architecture

The application follows a simple, self-contained architecture:

- **Single File Application**: Everything is in `index.html` (HTML + CSS + JavaScript)
- **No Dependencies**: Zero external libraries or frameworks
- **No Build Process**: Can be edited and viewed directly
- **Quiz Logic**: 20 hardcoded questions about JavaScript Date parsing edge cases
- **State Management**: Simple JavaScript variables track current question and score
- **User Interface**: Dark theme with keyboard shortcuts (1-4 for answers, Enter/Space for next)

## Key Code Sections

1. **Questions Array** (line ~274): Contains all quiz questions with code examples and multiple choice answers
2. **Quiz Logic** (line ~516+): Functions for displaying questions, handling answers, and tracking progress
3. **Event Handlers**: Keyboard shortcuts and button click handlers
4. **Share Functionality**: Uses Web Share API with clipboard fallback

## Deployment

The site can be deployed to any static hosting service (GitHub Pages, Netlify, Vercel, etc.) by simply uploading the `index.html` file. No build or compilation step is required.

## Testing Note

The project has no automated tests. Any changes should be manually tested by:
- Completing the quiz flow
- Testing keyboard shortcuts
- Verifying mobile responsiveness
- Checking share functionality