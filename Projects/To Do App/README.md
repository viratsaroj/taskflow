# Taskflow

Taskflow is a focused, responsive todo application for planning daily work. It runs entirely in the browser and stores tasks locally on the current device.

## Features

- Create and edit tasks
- Mark tasks complete or incomplete
- Delete tasks with undo support
- Clear completed tasks with undo support
- Assign categories: Work, Personal, Health, and Learning
- Set low, medium, or high priority
- Add due dates and recurring schedules
- Search tasks by title, category, or priority
- Filter by view, priority, or category
- Sort by date added, due date, priority, or title
- Responsive desktop and mobile layout
- Keyboard focus states and accessible control labels
- Reduced-motion support

## Technology

- Semantic HTML5
- Modern CSS3
- Vanilla JavaScript
- Browser `localStorage`
- No framework, build tool, backend, or runtime dependency

## Project Structure

```text
.
├── index.html   # Application markup and controls
├── style.css    # Design system and responsive layout
├── script.js    # State, rendering, task actions, and persistence
└── README.md    # Project documentation
```

## Run Locally

No installation is required. Open `index.html` directly in a browser.

For a local static server, use Node.js:

```powershell
npx serve .
```

Then open the URL shown by the command.

Alternatively, with a Python installation:

```powershell
python -m http.server 4173
```

Open `http://localhost:4173` in a browser.

## Data Storage

Tasks are saved under the `taskflow.tasks.v1` key in browser `localStorage`. Data is local to the browser and device. There is no account system, server database, or cross-device synchronization.

Clearing browser storage will remove saved tasks. Do not use this version for sensitive information.

## Deployment

Because Taskflow is a static frontend, it can be deployed to services such as:

- GitHub Pages
- Netlify
- Cloudflare Pages

Upload or connect the project directory as a static site. No build command is required.

## Validation

The available checks include:

```powershell
node --check script.js
```

The app can also be smoke-tested through a static server by confirming that `index.html`, `style.css`, and `script.js` load successfully.

## Current Limitations

- Persistence is browser-local only.
- There is no authentication or cloud synchronization.
- Browser interaction testing is currently manual.
- Recurring-task edge cases such as month-end dates need further hardening.
