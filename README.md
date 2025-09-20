# MSE Practice (Horizontal Line y = b)

A lightweight, front-end only web app for students to practice computing Mean Squared Error (MSE) for a set of points against a horizontal line y = b. No frameworks, a single `index.html` in the repo root.

## How to use

1. Open `index.html` directly in your browser (double-click it, or drag-drop into a tab).
2. You will see:
	- A plot with a set of randomly generated points (usually 2, sometimes 3–4) and the horizontal line `y = b`.
	- The exact coordinates and the value of `b` listed on the right.
3. Compute the MSE = average of `(y - b)^2` for all displayed points, enter your result, and click Check.
4. Click Reveal to see the step-by-step squared errors and the final MSE.
5. Click New to generate a fresh problem.

## Notes

- Point count distribution: 30% two points, 60% three points, 10% four points.
- Coordinates are small integers for mental math practice. The app avoids trivial cases (not all y are the same).
- Input checking uses a tight tolerance (1e-6). If you expect rounding, enter more decimals.
- The canvas auto-scales and draws a simple grid and axes for orientation.

## Customization

Open `index.html` and tweak these parts in the `<script>`:

- `weightedCount()` to change the two/three/four-point probabilities.
- `genPoints(n)` and the `randInt` ranges to expand the coordinate ranges.
- Tolerance in `approxEqual(val, current.mse, 1e-6)`.

## Attribution

Inspired by the instructor’s practice materials and repositories.