# Two-observer spacetime-diagram tool

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/daanmeerburg/WBPH001-10-Lectures/blob/main/Diagram_Tool/Two_Observer_Diagram_Tool.ipynb)

Click the button above to open `Two_Observer_Diagram_Tool.ipynb` in Google Colab without installing anything. The notebook creates correctly scaled two-observer **hyperbolic paper** in `(ct,x)` coordinates and includes helpers for events, worldlines, light rays, labels, ticks, and simple train/world-tube regions.

Set `beta = u/c` in the configuration cell. Its `size`, `symmetric`, `origin`, and `grid_dimensions` variables control the paper geometry. The faint hyperbolae are curves of constant Minkowski interval; the tilted axes and their tick positions are calculated from the Lorentz transformation, rather than chosen by eye. Use `fig.savefig("my_diagram.svg", bbox_inches="tight")` to export a vector graphic for LaTeX or slides.
