Here is a **clean, compact, README-ready version** of your module breakdown, fully reformatted and without unnecessary spacing:

---

# 🌀 Kolam Digitization & Grammar Extraction System

A modular pipeline to convert raw Kolam images into structured grammar rules and regenerate clean, digital Kolam patterns.

---

## 🔹 Module 1: Preprocessing & Grid Extraction

**Goal:** Identify dot positions & grid structure from raw Kolam images.

**Techniques:**

* Gaussian blur
* Adaptive thresholding
* OpenCV blob detection
* Hough circle detection

**Outputs:**

* Dot coordinates
* Grid structure (rows, columns, spacing)
* Dot density & grid symmetry

---

## 🔹 Module 2: Stroke & Curve Tracing

**Goal:** Convert Kolam strokes into vector paths.

**Techniques:**

* Canny edge detection
* Morphological thinning (skeletonization)
* Pixel-to-path tracing
* Conversion to cubic Bézier curves & splines

**Outputs:**

* Stroke graph (nodes + edges)

---

## 🔹 Module 3: Pattern Principle / Grammar Extraction

**Goal:** Extract reusable Kolam “grammar”.

**Detected Elements:**

### Symmetry Rules

* Rotational (90°, 180°, 360°)
* Reflectional
* Glide reflection

### Repetition Rules

* Grid-based motif repetition
* Curve template reuse
* Loop patterns

### Grammar Types

* L-system–style rules
* CFG-like rules
* Kolam Meta-Rules:

  * Around-dot loops
  * Between-dot arcs
  * Dot-avoiding strokes

### Output Format (KGF – Kolam Grammar File)

```json
{
  "grid": { "rows": 5, "cols": 5, "spacing": 20 },
  "symmetry": "D4",
  "motifs": ["loop", "arc", "double-arc"],
  "rules": ["F+F-F", "A -> ABA", "B -> F-F+F"]
}
```

---

## 🔹 Module 4: Rule Generator & Storage

**Goal:** Store, organize, and version grammar rules.

**Features:**

* Version control for rule evolution
* Grouping into rule families
* Categorization by pattern type
* Export to JSON / YAML / XML

---

## 🔹 Module 5: Kolam Reconstructor

**Goal:** Recreate Kolam using extracted grammar + geometry.

**Rendering Options:**

* Python Turtle
* Matplotlib
* SVG (Cairo)
* Pygame

**Outputs:**

* Clean digital Kolam
* Stepwise animation
* Pattern variations via rule tweaks

---

## 🔹 Module 6: UI / Frontend

**Goal:** Provide an intuitive interface for users.

**Features:**

* Image upload
* Dot extraction preview
* Stroke tracing visualization
* Grammar rule display
* Regenerate Kolam
* Generate variations
* Export images / videos

**Tech Options:**

* **Streamlit** (fastest dev)
* **Flask + React** (polished UI)

---
