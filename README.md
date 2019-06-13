# AJKF2019PaperSims

IMPORTANT NOTE: the meshes are provided in the google drive repository: https://drive.google.com/open?id=1HQYbxDbvYsOYF5nUQKQzuub1izK62aKH
If concerned about link security email to ihalayeto@gmail.com and request a new link.

Clone this repository and uncompress the meshes from Google drive on the same folder.
To create a case run the provided create$CASE script.
The turbulence model must be changed manually in the file /$CASE/constant/turbulenceProperties .
Sometimes a coarse mesh would stop or give a warning in a checkMesh run. Simply run the next line:
  transformPoints -scale '(1 1 0.01)'
to fix the issue.

Note that the simulations were run with OpenFOAM v4.1. Changes in format in further versions may require minor changes in dictionaries or function calls.

The postprocessing script readForcesTurbine.py is suggested to be run with Spyder. Copy on the folder /$CASE/ and run it.
The postprocessing script requires that:
  * the path should not be changed, i.e.: do not remove "coarse" nor "backward" from the path.
  * the function object names forcesBlade$NUMBER should not be changed.
There is a known issue if simulations are stopped with ctrl+C or the computer crashes while it is writing the file /$CASE/postProcessing/forcesBlade$NUMBER/$file . If the last line of the file is not complete remove it manually.
