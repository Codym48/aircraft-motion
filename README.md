Attempting to find the best combination of two tools:
 - Doxygen for overall project documentation
 - Jupyter Notebook for quick interactive visualizations

Generate the Doxygen `html` documentation package:

    doxygen Doxyfile

Will Jupytext allow us to keep these files in sync?

Synced   | File                         | Description                        | Links to Doxygen Output
---------|-----------------------------|------------------------------------|---------------
Manually | coordinate-frames.dox        | Doxygen C-style comment file       | [.html page name](coordinate-frames-dox.html) and [\\ref command](\ref coordinate-frames-dox)
Manually | coordinate-frames.doxygen.md | Doxygen Markdown format            | [.html page name](md_coordinate-frames_8doxygen.html) and [.md file name](coordinate-frames.doxygen.md)
Jupytext | coordinate-frames.ipynb      | Jupyter Notebook for interaction   ||
Jupytext | coordinate-frames.md         | Jupytext (GitHub?) Markdown format ||
Jupytext | coordinate-frames.py         | Python script                      ||


## Dependencies

Software           | Source
-------------------|----------
Anaconda 3 2020.02 | [Anaconda3-2020.02-Windows-x86_64.exe](https://repo.anaconda.com/archive/Anaconda3-2020.02-Windows-x86_64.exe)
Jupytext 1.4.2     | `conda install -c conda-forge jupytext`
Doxygen 1.8.18     | `conda install -c conda-forge doxygen`
MikTeX 2.9.6753    | `conda install -c conda-forge MikTeX`
GhostScript 9.22   | `conda install -c conda-forge GhostScript`
