# AJKF2019PaperSims

IMPORTANT NOTE: the meshes are provided in the google drive repository: https://drive.google.com/open?id=1HQYbxDbvYsOYF5nUQKQzuub1izK62aKH
If concerned about link security email to ihalayeto@gmail.com and request a new link.

Clone this repository and uncompress the meshes from Google drive on the same folder.
To create a case run the provided create$CASE script.
The turbulence model must be changed manually in the file /$CASE/constant/turbulenceProperties .
Sometimes a coarse mesh would stop or give a warning in a checkMesh run. Simply run the next line:
  transformPoints -scale '(1 1 0.01)'
to fix the issue.
