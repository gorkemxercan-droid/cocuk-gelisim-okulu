# System Patterns

## Architecture
-   **Static Site**: The project is a collection of static HTML files.
-   **No Build Step**: Currently running directly in the browser.
-   **Styling**: TailwindCSS via CDN (`cdn.tailwindcss.com`).
    -   *Risk*: CDN usage is fine for dev/demos but a build step is recommended for production performance and caching.
-   **Scripts**: Embedded JavaScript for Tailwind config and minor interactivity.

## Design Patterns
-   **Tailwind Config**: Defined strictly within the `<script>` tag in the `<head>` of each file.
    -   *Duplication Warning*: The Tailwind config is duplicated across files. Changing a color requires editing every file.
    -   *Recommendation*: Move to a shared `config.js` or build process.

## Code Structure
-   `*.html`: Contains Structure (HTML) + Style (Tailwind classes) + Logic (Inline JS).
-   **Assets**: Images are currently hosted externally (Google/Aida public links) or embedded.
