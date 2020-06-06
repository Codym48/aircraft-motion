Attempting to find the best combination of two tools:
 - Doxygen for overall project documentation
 - Jupyter Notebook for quick interactive visualizations

Given an .ipynb file with LaTeX equations, I paired it with .py and .md
files using Jupytext. I manually created a [Doxygen C-style comment
file](http://doxygen.nl/manual/docblocks.html#cppblock), a [Doxygen Python
comment file](https://www.doxygen.nl/manual/docblocks.html#pythonblocks),
and a [Doxygen Markdown file](http://doxygen.nl/manual/markdown.html)
that contain the same content but have been updated to correctly render
Doxygen .html pages with LaTeX equations. To generate the Doxygen `html`
documentation package, call:

    doxygen Doxyfile

Would Jupytext allow us to automatically keep any of these* files in sync?

Synced   | File                         | Description                        | Links to Doxygen Output                                                                                 | Diff From Jupytext .md
---------|------------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------
Manual*  | coordinate-frames.dox        | Doxygen C-style comment file       | [.html page name](coordinate-frames-dox.html) and [\\ref command](\ref coordinate-frames-dox)           | See d94e14c3 message
Manual*  | coordinate-frames.doxygen.md | Doxygen Markdown format            | [.html page name](md_coordinate-frames_8doxygen.html) and [.md file name](coordinate-frames.doxygen.md) | See 52d6fc13 message
Manual*  | coordinate-frames.doxygen.py | Python script with Doxygen comments| [.html page name](modules.html) | See 2e55cf0 message
Jupytext | coordinate-frames.ipynb      | Jupyter Notebook for interaction   |||
Jupytext | coordinate-frames.md         | Jupytext (GitHub?) Markdown format |||
Jupytext | coordinate-frames.py         | Python script                      |||

## Dependencies

Software           | Source
-------------------|----------
Anaconda 3 2020.02 | [Anaconda3-2020.02-Windows-x86_64.exe](https://repo.anaconda.com/archive/Anaconda3-2020.02-Windows-x86_64.exe)
Jupytext 1.4.2     | `conda install -c conda-forge jupytext`
Doxygen 1.8.18     | `conda install -c conda-forge doxygen`
MikTeX 2.9.6753    | `conda install -c conda-forge MikTeX`
GhostScript 9.22   | `conda install -c conda-forge GhostScript`
