# Two-observer spacetime-diagram tool

Open `Two_Observer_Diagram_Tool.ipynb` in [Google Colab](https://colab.research.google.com/) (or Jupyter) and run the cells from top to bottom. The notebook creates a correctly scaled two-observer diagram in `(ct,x)` coordinates and includes helpers for events, worldlines, light rays, labels, ticks, and simple train/world-tube regions.

Set `beta = u/c` in the configuration cell. The tilted axes and their tick positions are calculated from the Lorentz transformation, rather than chosen by eye. Use `fig.savefig("my_diagram.svg", bbox_inches="tight")` to export a vector graphic for LaTeX or slides.
