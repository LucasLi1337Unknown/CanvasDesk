# CanvasDesk

A lightweight visual workspace for sketching, diagrams, notes and ideas. Built with plain HTML, CSS, JavaScript and SVG. No account, build step, API key, analytics or third-party runtime dependencies.

## Features

- Freehand pen, rectangles, ellipses, lines and arrows
- Multiline text and sticky notes; double-click to edit
- Move, resize, duplicate, delete and reorder individual objects
- Color, fill, stroke width and text-size controls
- Image import (PNG, JPEG, WebP and GIF, flattened into a still image)
- Pan, zoom, fit-to-content and undo/redo
- Automatic saving in the current browser
- PNG and SVG download, optionally with a transparent background
- Editable `.canvasdesk` board download and import for sharing with friends
- Responsive layout and touch drawing

## Run

Open `index.html` in a modern browser, or serve this directory using any static host.

For GitHub Pages, choose **Settings → Pages → Deploy from a branch → main → / (root)**. No Actions workflow or build dependencies are required.

## Shortcuts

| Key | Action |
| --- | --- |
| V / H | Select / pan |
| P / R / O | Pen / rectangle / ellipse |
| A / L / T / N / E | Arrow / line / text / note / erase |
| Space + drag | Pan |
| Mouse wheel | Zoom around the pointer |
| Ctrl or Command + Z | Undo |
| Ctrl or Command + Shift + Z | Redo |
| Ctrl or Command + D | Duplicate selection |
| Delete / Backspace | Delete selection |
| Arrow keys / Shift + arrow keys | Move selection 1 / 10 units |

## Data and sharing

Boards stay in the current browser's local storage. They are not uploaded to GitHub or a server. Download an editable board as a backup, particularly before clearing browser data or working with many images. To share a drawing, send its PNG/SVG or send the editable board file and ask the recipient to open it in CanvasDesk. This version does not offer live collaboration or cross-device sync.

Image imports are resized to at most 1600 pixels per side. Input images are limited to 6 MB, board imports to 15 MB and 5,000 objects. PNG export is capped to 24 megapixels and 8192 pixels per side; SVG remains scalable. Text is plain text, never interpreted as HTML. Imports only allow embedded raster images, not remote images or embedded SVG scripts.

## Verification

Automated DOM checks cover drawing, shape creation, object movement, undo/redo, duplication/deletion, multiline text escaping, saved-board validation, SVG content and rejection of remote image imports. Browser visual checks and real PNG downloads require a full browser.
