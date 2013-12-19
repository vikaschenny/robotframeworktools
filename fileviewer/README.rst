=============
fileviewer.py
=============

``fileviewer.py`` is a tool for viewing Robot Framework debug files. It can be
downloaded here__.

__ https://bitbucket.org/robotframework/robottools/raw/master/fileviewer/fileviewer.py

Synopsis
========
.. sourcecode:: bash

    $ fileviewer.py [debugfile]


Description
===========

File viewer is a tool designed to be used together with the Robot
Framework command line option: *--debugfile*. The debug file can be
opened with File viewer, and the viewer will automatically update the
display as the debug file gets written, so that it is possible to
scroll the file when it is being written to.

To use the tool, you can either double-click the icon and click the
``Open`` button in the GUI to open the desired file, or you can start
the tool from the command line and give the path to the debug file as
an argument, for example::

   python fileviewer.py mydebugfile.txt

.. figure:: http://bitbucket.org/robotframework/robottools/raw/master/fileviewer/fileviewer.png
   :width: 754
   :height: 521

   File viewer

