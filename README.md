# Mini‑CAD 2D (Compatibility Pro)

A single‑file, AutoCAD‑style 2D CAD tool that runs locally in any modern browser — no build, no server, no dependencies.  
**Features:** grid/axes, pan/zoom, Zoom Extents/Window/Previous, command line (LINE, PLINE, REC, C, M, CO, RO, SC, E, Z), snaps (Grid/End/Mid/Int), Ortho (F8), layers, grips, modify tools (Move/Copy/Rotate/Scale), DXF (R12 LINEs) + JSON I/O. Designed with old‑school JS for maximum compatibility.

## Quick start
1. Download **`mini-cad.html`** and open it in your browser (double‑click).  
2. If you see a blank view, click **Reset View** then **Force Redraw**, or **Test Pattern** to draw a square.  
3. Draw: click **Line** (or type `LINE` + Enter) and pick two points.
4. Pan/Zoom: middle/right drag or **Pan**; use mouse wheel/pinch to zoom.
5. Export: click **DXF** for R12 DXF; **Save** for JSON.  
6. Import: **Open** accepts `.json` or `.dxf` (R12 LINE segments).

## Keyboard & Commands
- **Space** repeats last command. **Esc** cancels.
- **F8** toggles Ortho.  
- **Ctrl/⌘+S** save JSON. **Ctrl/⌘+O** open.  
- Commands: `LINE, PLINE, REC, C, M, CO, RO, SC, E, Z`  
  - `Z E` extents, `Z P` previous, `Z W` window
  - `RO` rotate: pick base, type angle or second point
  - `SC` scale: pick base, type factor or second point

## Files
- `mini-cad.html` — the whole app (open directly in the browser)
- `LICENSE` — MIT
- `CHANGELOG.md` — release notes
- `CONTRIBUTING.md` — how to contribute
- `.gitignore` — typical web/dev ignores

## Dev notes
- Pure ES5‑style JS: no arrow functions, optional chaining, PointerEvents, etc.
- Canvas drawing uses devicePixelRatio but clears under identity transform to avoid artifacts.
- DXF output: R12 `LINE` entities from poly segments; circles are approximated with 64‑seg polygons.
- Intersection/mid/end snaps implemented; intersection tests only for segments near cursor for performance.

## Roadmap ideas
- Text & dimensions; arcs/fillets; trim/extend; offset
- Better DXF import (ARC, LWPOLYLINE); DXF color by layer
- Persistent settings (localStorage)
- Unit settings & measurement readout; length/angle input on command line
- Export SVG/PNG

---
If you hit issues on a specific browser/device, please open an issue with a screenshot and the red error box text from the app.
