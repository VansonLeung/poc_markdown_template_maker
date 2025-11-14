# VANPORT WYSIWYG — AI-Assisted HTML WYSIWYG Studio

## (TODO: AI assistance features coming soon)

VANPORT WYSIWYG is a single-page, desktop-first playground powered by vanilla JavaScript and TailwindCSS (via CDN). It blends rich authoring tools with AI-friendly workflows so you can craft, reuse, and share polished HTML templates without leaving the browser.

## Key Features
- **Modern editor canvas** – `contenteditable` stage with typography presets, responsive padding, and inline highlighting.
- **Context + global tooling** – floating formatting bubble near selections, primary toolbar for rich-text commands, and quick sharing/export buttons.
- **Layout builders** – sidebar presets insert one-, two-, or three-column flex layouts; dedicated inspector lets you tweak direction, alignment, wrapping, and gap without touching CSS.
- **Table studio** – generate tables with arbitrary rows/columns, merge/split support stubs, size inputs, and per-cell styling controls.
- **Template system** – save/load snippets to `localStorage`, export JSON payloads, or copy the generated HTML/DOM code directly.
- **Preview + share** – live preview dialog with desktop/tablet/mobile widths, copy-to-clipboard HTML/JSON, and quick Whatsapp/email share helpers.
- **Dark theme toggle** – persistent (localStorage) theme switch honoring system preferences and updating the preview frame.

## Repository Layout
```
index.html          # Main application (all UI/logic/styles live here)
docs/20251114/      # Product background, requirements, and planning notes
README.md           # You are here
```

## Getting Started
1. **Clone or download** this repo.
2. **Open `index.html`** directly in any modern browser (Chrome, Edge, Firefox, Safari). No build step required.
3. Optionally run a static server (e.g. `npx serve .`) if you prefer consistent localStorage origins while iterating.

## Usage Notes
- Use the left “Layout Blueprints” panel to inject flex presets and the “Table Studio” section to insert/edit tables.
- Select any element in the editor to see contextual controls (table inspector, flex inspector, floating bubble).
- The header buttons let you copy HTML, share, open live preview (with different device widths), view/code-edit the markup, and toggle light/dark.
- Saved templates, preview device sizes, and active theme persist in browser `localStorage` under `proton-*` keys.

## Extending the Project
- **Styling:** Tailwind is loaded via CDN for utility classes while core layout styles live in the `<style>` block inside `index.html`. Extract to separate CSS if the project grows.
- **Components/JS:** All logic currently sits in an IIFE near the bottom of `index.html`. Consider modularizing as ES modules if additional features (LLM APIs, richer drag/drop, etc.) are added.
- **APIs / Automation:** Product goals in `docs/20251114/*.md` outline desired template APIs for LLM workflows. Use those notes as a roadmap for backend/service work.

## Roadmap & Ideas
- Turn template persistence into real storage (REST/GraphQL) to enable collaboration and LLM programmatic access.
- Add drag-to-resize for rows/columns and flex handles.
- Support custom placeholder tags plus validation before export.
- Harden copy/paste formatting and add undo/redo history visualization.

Feel free to open issues or PRs as you expand VANPORT WYSIWYG!
