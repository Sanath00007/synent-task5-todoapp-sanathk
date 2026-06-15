# Orbit — To-Do App

A clean, fast, dependency-free to-do list app for staying on top of your day. Built with plain HTML, CSS, and JavaScript — no frameworks, no build step, no external runtime dependencies.

## Features

- **Add, edit, complete, and delete tasks** with inline editing
- **Priority levels** — High, Medium, Low — each with its own color accent
- **Filters** — view All, Pending, or Completed tasks
- **Live search** — instantly filter tasks by keyword
- **Stats bar** — total, done, and pending counts with a progress bar
- **Clear All** with a confirmation modal to prevent accidental wipes
- **Light / Dark mode** with a one-click toggle (preference is remembered)
- **Live date & time display** in the header
- **Toast notifications** for add, complete, edit, delete, and clear actions
- **Persistent storage** — tasks and theme are saved in the browser via `localStorage`
- **Keyboard support** — `Enter` to add or save, `Escape` to cancel an edit or close the modal
- **Accessible** — semantic markup, ARIA labels, focus states, and `prefers-reduced-motion` support
- **Responsive** — works on desktop and mobile screen sizes

## File Structure

```
.
├── index.html   # App markup / structure
├── style.css    # Styling, theming (light & dark), animations
└── script.js    # App logic, state management, and persistence
```

## Getting Started

No installation or build tools required.

1. Download/clone the three files (`index.html`, `style.css`, `script.js`) into the same folder.
2. Open `index.html` in any modern web browser.

That's it — the app runs entirely client-side.

## Usage

- **Add a task**: Type into the input field, choose a priority (High / Medium / Low), and press `Enter` or click **Add**.
- **Complete a task**: Click the checkbox next to a task.
- **Edit a task**: Click the edit (pencil) icon, update the text, then press `Enter` or click the save icon. Press `Escape` to cancel.
- **Delete a task**: Click the trash icon.
- **Search**: Type in the search bar to filter tasks by text in real time.
- **Filter**: Use the **All / Pending / Completed** tabs to narrow the list.
- **Clear all tasks**: Click **Clear all** and confirm in the dialog. This cannot be undone.
- **Toggle theme**: Click the sun/moon icon in the top right to switch between light and dark mode.

## Data Persistence

All tasks and your theme preference are stored locally in your browser's `localStorage` under the keys:

- `orbit_tasks` — your task list (JSON)
- `orbit_theme` — `light` or `dark`

No data is sent to a server. Clearing your browser storage for this page will reset the app.

## Customization

- **Colors & theming**: All design tokens (colors, radii, shadows, transitions) are defined as CSS custom properties at the top of `style.css` under `:root` and `[data-theme="dark"]`. Adjust these to change the look across the whole app.
- **Fonts**: Headings use **Space Grotesk**, body text uses **Inter** (loaded via Google Fonts in `index.html`).
- **Priority colors**: Controlled by the `--red`, `--amber`, and `--blue` tokens for High, Medium, and Low respectively.

## Browser Support

Works in all modern evergreen browsers (Chrome, Edge, Firefox, Safari) that support CSS custom properties, `:has()`, and `localStorage`.

## License

Free to use, modify, and distribute for personal or academic projects.
