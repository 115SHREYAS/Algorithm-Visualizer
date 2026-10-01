# AGENTS.md

## Project overview

This is a static algorithm visualizer built with HTML, CSS, and browser JavaScript. There is no package manager, build step, or automated test suite configured.

## Project layout

- `index.html` and `style.css` provide the home page and navigation.
- `Sorting/sorting.html` is the sorting visualizer page. Its behavior is in `Sorting/sorting.js` and the algorithm files `bubble.js`, `selection.js`, `insertion.js`, `merge.js`, and `quick.js`; page styles are in `sorting.css`.
- `Searching/searching.html` is the searching visualizer page. Its behavior is in `Searching/searching.js`, `LinearSearch.js`, and `Binary.js`; page styles are in `searching.css`.
- Each visualizer folder also contains Prism assets and audio files used by its page.

## Working conventions

- Keep this project dependency-free unless a change clearly requires adding a tool.
- Preserve the existing plain JavaScript and CSS approach. There is no module or bundler setup; page scripts are loaded with `<script>` tags, and their order can matter because the visualizers share globals and DOM state.
- Keep asset paths relative to the HTML file that uses them. File and directory names are case-sensitive; preserve existing capitalization such as `Searching/` and `Sorting/`.
- When changing visualizer controls or markup, check the corresponding JavaScript selectors and event handlers so element IDs and classes stay in sync.
- Keep sorting and searching implementations in their respective folders. Update the matching HTML page when adding or removing a script or stylesheet.

## Running and checking changes

- Open `index.html` in a browser, or serve the project root with a static HTTP server and navigate to `/`. No build command is needed.
- For UI or algorithm changes, manually exercise the affected page and controls in a browser. Check the browser console for JavaScript errors and verify that navigation and local assets load.
- There is no configured test or lint command. Do not assume one exists unless project tooling is added.
