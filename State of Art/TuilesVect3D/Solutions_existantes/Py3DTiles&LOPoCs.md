# Py3DTiles & LOPoCs

## py3dtiles


Source : http://www.oslandia.com/py3dtiles-en.html?utm_source=dlvr.it&utm_medium=twitter
<br/>
Date : November 2016

###### To use py3dtiles from sources

License : LGPL2 or later.


<pre>
<code>
$ git clone https://github.com/Oslandia/py3dtiles
$ cd py3dtiles
$ virtualenv -p /usr/bin/python3 venv
$ . venv/bin/activate
(venv)$ pip install -e .
(venv)$ python setup.py install
</code>
</pre>

###### Read/Write .pnts file

https://pypi.python.org/pypi/py3dtiles/
<br/>
https://github.com/Oslandia/py3dtiles/



Python module (in development) manage 3DTiles (just Point Cloud spec).
<br/>
py3dtiles is currently used by LOPoCS, a server streaming Point Cloud from Postgis, to send data to Cesium.


## LOPoCs

Source : https://github.com/LI3DS/lopocs : Installation, Use & API
<br/>
It is a Point Cloud server in Python and trhe only 3DTiles server.
It loads Point Cloud from Postgis (with pgpointcloud extension) in Cesium (3DTiles), iTowns2 (Greyhound), Potree viewer (Greyhound).


###### Greyhound format 
LAZ data with a footer indicating the number of points
- info: returns information about the dataset served by the server in JSON
- hierarchy: returns the description of the dataset according to an octree in JSON
- read: returns points in LAZ format

###### 3DTiles format
- info: returns information about the dataset in JSON
- read.pnts: returns points in 3DTiles Point Cloud format
