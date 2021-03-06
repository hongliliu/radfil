# RadFil
RadFil is a radial density profile building and fitting tool for interstellar filaments. All you need to build and fit a radial density profile for your own filaments is an image array and (in most cases) a boolean mask array delineating the boundary of your filament. RadFil can do the rest! Please see the tutorial (housed in RadFil_Tutorial.ipynb) for a complete working example of the code. 

Python2 vs. Python3
------------
*   While RadFil is written to be cross-compatible between python2 and python3, it relies on the FilFinder package to build filament spines via medial axis skeletonization of the filament masks. Since FilFinder is currently only compatible with python2 (support for python3 is planned in future) RadFil must be run in python2 if you do not already have a filament spine that has been precomputed for input into RadFil.


Installation
------------

RadFil can be installed via pip:

```
pip install radfil
```

To install from the repository, download the zip file from github and run the following in the top level of the directory:
```
python setup.py install
```

Package Dependencies
--------------------

Requires:

 *   numpy
 *   scipy
 *   matplotlib
 *   astropy
 *   shapely
 *   sklearn
 *   scikit-image
 *   networkx

Optional:

 *  fil_finder -- only required if you are *not* inputing a precomputed filament spine, and you want RadFil to use the fil_finder package to create one for you
 *  descartes -- only required if you do *not* input a filament mask, and you still want to shift the profile along each cut to the pixel with the peak column density
 
 Questions? Comments?
--------------------
The RadFil package has been developed by Catherine Zucker (catherine.zucker@cfa.harvard.edu) and Hope Chen (hhchen@cfa.harvard.edu). If you find a bug, have questions, or would like to request a new feature, please feel free to send us an email or raise an issue in the github repository. We'd love to hear from you!
