# tpms2path
## TPMS Slicing Visualization and G-code Generation

Jupyter notebook for generating toolpaths from Triply Periodic Minimal Surface (TPMS) structures.

The notebook supports:

* XY, XZ, and YZ slicing planes
* Optional angled slicing planes
* Multiple wall offsets along the surface normal
* Several TPMS surface types
    * schwarzP
    * gyroid
    * diamond
    * fischerkoch
    * iwp
    * splitP
* Configurable unit cell size and structure dimensions
* Visualization of generated toolpaths
* Optional G-code export using FullControl
* G-code metadata in the header
* Axis-specific path colors

## Requirements

Install the required Python packages:

```bash
pip install numpy matplotlib scikit-image fullcontrol
```

## Usage
Open `tpms2path.ipynb` in Jupyter Notebook or JupyterLab.

Adjust the parameters in the `PARAMETERS` section and run the notebook cells.

Set `plot_output = True` to display the 3D toolpath preview and `gcode_output = True` to export G-code.

The generated structure is centered at `X=0, Y=0`.

## G-Code compatibility
The generated G-code is intended for use with a specific printer and may not be compatible with other printing systems.

Before running the generated G-code, verify that the printer configuration, coordinate system, extrusion settings, and other machine-specific parameters are appropriate for the target printer.

Always inspect and validate the generated G-code before printing. The user is responsible for ensuring that the G-code is compatible with the intended printer.

## Acknowledgements

This project uses [FullControl](https://github.com/FullControlXYZ/fullcontrol)
for toolpath generation and G-code export.

Please cite the FullControl publication when using this work in academic
research:

Gleadall, A. (2021). FullControl GCode Designer: open-source software for
unconstrained design in additive manufacturing. Additive Manufacturing,
46, 102109. https://doi.org/10.1016/j.addma.2021.102109
