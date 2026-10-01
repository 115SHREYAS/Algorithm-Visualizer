# Algorithm Visualizer

A browser based learning tool for watching common sorting and searching algorithms run on an array. The visualizers animate the algorithm, show the current array, and provide Java code and complexity notes.

## Features

- **Sorting:** Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, and Quick Sort.
- **Searching:** Linear Search and Binary Search, with a search value field and results for the found position and step count.
- **Controls:** Generate a new random array, adjust its size, and change the animation speed.
- **Algorithm details:** View Java examples and time and space complexity information alongside the visualization.
- **Home page:** Navigate between the sorting and searching visualizers; toggle the page theme and navigation menu.

## Run locally

This is a static site; it has no build step or package dependencies. Clone or download the repository, then open `index.html` in a browser. For a local web server, run this command from the project directory:

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. The home page loads Ionicons from a CDN, so an internet connection is needed for those icons. You can also open the visualizers directly:

- `Sorting/sorting.html`
- `Searching/searching.html`

## Using the visualizers

1. Choose a visualizer from the home page (or open its HTML file directly).
2. Set the array size and animation speed with the sliders.
3. Click **Generate New Array** to create a fresh random array.
4. On the sorting page, select one of the five sorting algorithms. On the searching page, enter a value and choose Linear Search or Binary Search.
5. Review the code and complexity panels below the animation.

## Project structure

```text
.
├── index.html              # Home page and navigation
├── style.css               # Home page styles
├── Sorting/
│   ├── sorting.html        # Sorting visualizer interface
│   ├── sorting.js          # Array and control behavior
│   └── *.js                # Sorting algorithm implementations
└── Searching/
    ├── searching.html     # Searching visualizer interface
    ├── searching.js       # Array and control behavior
    └── *.js               # Search algorithm implementations
```

Stylesheets, Prism syntax highlighting assets, and sound effects are kept next to their corresponding visualizer. No compilation is required; serve the repository root so the relative asset paths continue to work.
