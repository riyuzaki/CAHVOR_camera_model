# CAHVOR_camera_model - Python Implementation
* Converting Photogrammetric Parameters to CAHVOR
* Python Implentation of [CAHVOR camera model and its photogrammetric conversion for planetary applications](http://onlinelibrary.wiley.com/doi/10.1029/2003JE002199/full)

Dependancies
------------
* Python3
* Numpy

CAHVOR model
------------
* CAHVOR camera model [details](http://pds-imaging.jpl.nasa.gov/data/mer/spirit/mer2no_0xxx/document/geometric_cm.txt)

Input
-----
Camera matrix parameters generated from camera calibration

(NOTE: User must have `EXTRINSIC` and `INTRINSIC` camera parameters generated from Camera Calibration)

Usage
-----

* Python3

  ```
  >>> from get_cahvor import PhotogrammetricModel
  >>> a = PhotogrammetricModel()
  >>> a.cahvor
  ```
* command-line

  ```
  $ python3 get_cahvor.py
  ```

Results
-------
$  python3 get_cahvor.py

```
--------------------------------------------------------------
Note: Enter Vector Elements Row by Row with Space in between
--------------------------------------------------------------

Enter Principal Point (x0, y0): -0.09574394 -0.11071695
Enter Image Size (Row, Column): 506 762
Enter Focal Length in mm: 29.4711992
Enter Camera Center (Xc, Yc, Zc): 3.451904 3.258335 1.254338
Enter pixel size in mm: 0.01838
Enter Rotation Angle w: -72.2993175
Enter Rotation Angle phi: 44.2841281
Enter Rotation Angle k: 166.5327547
Enter Distortion Parameters (k0, k1, k2): 0.0002 -0.00012443 0.00000011

--------------------------------------------------------------

hs:  1603.4384766050055
vs:  1603.4384766050055
hc:  375.79086289445047
vc:  259.0237731229597
C:  [3.451904, 3.258335, 1.254338]
A:  [-0.698217   -0.6819946  -0.21766119]
H:  [-1378.70002113   894.469724    -106.50767804]
V:  [   86.47420373    49.07120279 -1621.17935234]
O:  [-0.698217   -0.6819946  -0.21766119]
R:  [ 0.0002     -0.10807387  0.082982  ]

--------------------------------------------------------------
```
$ python3 get_photogrammetric_model.py
```
--------------------------------------------------------------
Note: Enter Vector Elements Row by Row with Space in between
--------------------------------------------------------------

Enter C Vector: 3.451904 3.258335 1.254338
Enter A Vector: -0.698217 -0.681994 -0.217661
Enter H Vector: -1378.872803 894.719666 -106.732689
Enter V Vector: 86.414558 49.038635 -1620.883789
Enter O Vector: -0.695858 -0.679843 -0.231508
Enter R Vector: 0.0002 -0.108075 0.086320
Enter pixel size in mm: 0.01838
Enter Image Size (Row, Column): 506 762
Enter hs: 1603.741455
Enter vs: 1603.1354
Enter hc: 375.790863
Enter vc: 259.023773

--------------------------------------------------------------

f:  29.476767942900004
Xc:  3.451904
Yc:  3.258335
Zc:  1.254338
x0:  -0.09574393805999998
y0:  -0.1107169477400001
Angle w (deg):  -72.29916094406916
Angle phi (deg):  44.28412812851018
Angle k (deg):  166.5245817162046
k0:  0.0002
k1:  -0.00012438428650870753
k2:  1.1433836611397755e-07

--------------------------------------------------------------
```
Reference
----------
* Di, Kaichang, and Rongxing Li. "CAHVOR camera model and its photogrammetric conversion for planetary applications." Journal of Geophysical Research: Planets 109.E4 (2004).
