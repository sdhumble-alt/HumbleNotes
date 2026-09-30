# A Humble Note Builder[cite: 2]
**Version:** 1.3.0 — 2026-09-20[cite: 2]
**Author:** Steven Humble[cite: 2]
**Suite:** "A Humble..." Educational Web Applications[cite: 2]

> **IMPORTANT NOTE:** Do not update the application version number until explicitly directed to do so by the user.[cite: 2]

## Overview
**A Humble Note Builder** is a client-side, single-page web application designed specifically for educators.[cite: 2] It solves the formatting frustrations of standard word processors by providing a free-form, mathematically scaled canvas optimized for creating guided notes, graphic organizers, and Interactive Student Notebook (ISN) inserts.[cite: 2] 

The application ensures that what is designed on the screen scales perfectly to physical paper, offering specialized tools like automated Cornell Notes layouts, smart alignment guides, and rich-text editing with built-in scientific symbols.[cite: 2]

---

## Core Features

### 1. Precision Canvas & Layout Engine
* **Custom Dimensions:** Built-in presets for Standard Letter (8.5" x 11") and Composition Notebooks (6.25" x 8.5" & 7" x 9"), plus custom inch-based inputs.[cite: 2]
* **Orientation:** One-click toggling between Portrait and Landscape, remembered locally.[cite: 2]
* **Intelligent Scaling:** Custom 3-way confirmation modal (*Yes, scale*, *No, do not scale*, *Cancel*) when changing paper dimensions with existing content.[cite: 2]
* **Smart Snapping:** Elements automatically snap to a customizable pixel grid or to the edges/centers of other elements via magenta Smart Guides (active on both drag and resize).[cite: 2]
* **Auto-Fit Viewport:** The canvas automatically defaults to 100% zoom or "fit width" on load, whichever is smaller.[cite: 2]

### 2. Element Library
* **Properties Panel:** Context-aware "Element Properties" panel intelligently docks at the top of the controls sidebar the moment an element is selected.[cite: 2]
* **Blank Boxes:** Resizable containers that support independent, locally-saved line spacing (default 20px) and grid spacing (default 14px), and inline Header Labels with Left, Center, or Right justification.[cite: 2]
* **Text Blocks:** Borderless floating text zones.[cite: 2]
* **Ellipses:** Circular or oval shapes that support solid or transparent backgrounds and centered text.
* **Lines / Arrows:** Horizontal, vertical, and diagonal lines with smart auto-flipping logic and configurable arrowheads (None, End, Both).
* **Data Tables:** Highly customizable grids where rows and columns can be scaled.[cite: 2] Newly inserted tables default to Center and Middle alignment, with the first row automatically bolded.[cite: 2] Users can toggle formatting targets between the entire table or specific focused cells.
* **Images:** Local file uploads that scale proportionally.[cite: 2]
* **Page Numbers:** Auto-calculates the bottom-right corner of the safe zone to drop a 9pt centered page number block.[cite: 2]

### 3. Graphic Organizers & Templates
* **Static Templates with Guiding Headers:**
  * **Cornell Notes:** Instantly generates a mathematically scaled, 4-part layout (Topic / Objective, Questions / Cues, Notes, Summary).[cite: 2]
  * **Frayer Model:** Auto-generates a 5-part vocabulary matrix (Definition, Characteristics, Examples, Non-Examples, Topic / Word).[cite: 2]
  * **Science Lab Protocol:** Auto-generates a dynamically scaled, proportional layout featuring reading sections and open workspace boxes for data collection (Lab Title, Question / Purpose, Variables, Hypothesis, Procedure & Data, Observations, Analysis, Conclusion).[cite: 2]
  * **KWL Chart:** 3-column chart for tracking learning stages (What I Know (K), What I Wonder (W), What I Learned (L)).
  * **Concept Map:** Hierarchical flowchart mapping a central idea to sub-points (Main Concept, Detail, Detail / Example, Synthesis / Summary).
* **Static Templates (Unlabeled):**
  * **T-Chart & Venn Diagram:** Unlabeled 2-column comparison layout or intersecting ellipses.
  * **Fishbone Diagram:** Cause-and-effect layout featuring a spine and intersecting bone boxes.
* **Dynamic / Configurable Templates:** Features an "Edit Organizer Structure" button in the properties panel to dynamically update the layout on the fly.
  * **Bubble & Double Bubble Maps:** Configurable count of detail and shared attribute bubbles.
  * **Flow & Cyclical Maps:** Configurable count of sequential or circular stages.
  * **Tree & Brace Maps:** Configurable subtopics, major parts, and subparts.
  * **Storyboard Grid:** Configurable rows and columns, featuring a drawing box and a lined text box per cell.

### 4. Advanced Text & Formatting
* **Global Typography:** Select a master font (saved locally) that applies to the entire document.[cite: 2] The base font size for all new elements defaults to 12pt.[cite: 2]
* **3-Tier Rich Text Toolbar:** Cleanly organized into three distinct rows for rapid formatting:[cite: 2]
  * *Row 1:* Font Size, Bold, Italic, Underline, Strikethrough.[cite: 2]
  * *Row 2:* Math/Greek symbol insertion, Subscript/Superscript (which toggle on and off for all selected text), and List toggles.[cite: 2]
  * *Row 3:* Horizontal and Vertical alignment controls.[cite: 2]
* **List Engine:** Auto-incrementing Bullet, Numbered, Outline, and Checkbox (`☐`) lists featuring automatic word-processor style line continuation and hanging indents.[cite: 2]
* **Scientific Notation:** Dedicated insertion panels for Greek letters and Math symbols, plus multi-character Subscript and Superscript toggling.[cite: 2]

### 5. Project Management & Export
* **.humblenote Files:** Save and open ongoing projects as lightweight local JSON files.[cite: 2]
* **History Stack:** Full Undo/Redo tracking for all canvas actions.[cite: 2]
* **Local Storage:** Remembers paper size, orientation, custom dimensions, font family, and line/grid spacing preferences.[cite: 2]
* **High-Fidelity PDF Export:** Utilizes `jsPDF` to generate resolution-perfect PDF files with cutting guide tick-marks for non-standard paper sizes.[cite: 2]

---

## Technical Architecture

* **Frontend Structure:** HTML5 & CSS3, utilizing CSS Grid and Flexbox.[cite: 2]
* **Rendering Engine:** HTML5 `<canvas>` API (`CanvasRenderingContext2D`) for drawing, text wrapping, and bounding boxes.[cite: 2]
* **Dependencies:** Tabler Icons, jsPDF.[cite: 2]

---

## Keyboard Shortcuts

| Shortcut | Action | Scope |
| :--- | :--- | :--- |
| `Backspace` / `Delete` | Delete Element | Canvas (when element selected, not typing)[cite: 2] |
| `Ctrl + C` / `Cmd + C` | Copy Element | Canvas[cite: 2] |
| `Ctrl + X` / `Cmd + X` | Cut Element | Canvas[cite: 2] |
| `Ctrl + V` / `Cmd + V` | Paste Element | Canvas (Pastes with a 20px offset)[cite: 2] |
| `Ctrl + Scroll Wheel` | Zoom Canvas | Viewport[cite: 2] |
| `Enter` | Next List Item | Textarea (auto-increments list markers)[cite: 2] |
