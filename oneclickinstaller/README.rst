===================================
Robot Framework One Click Installer
===================================

An AutoIT_ script for installing `Robot Framework`_ and its preconditions
on Windows XP machines. The installer executable can be downloaded from
`project downloads`__.

__ https://bitbucket.org/robotframework/robottools/downloads


Description
===========

The One Click Installer installs Robot Framework and its preconditions
Python_ and Jython_ (optional). It also sets Robot Framework start-up
scripts (``pybot``, ``jybot``, ``rebot``), as well as Python and Jython
executables, into the ``%PATH%`` environment variable, so that they can be
executed from the command line. Note that you need to restart the
command prompt for these changes to take effect. You should use this
installer *ONLY* if you do not previously have Python or Jython
installed. In that case, and also if you want to have a custom
installation, you need to install the needed components separately.

    **Note:**
        The One Click Installer works only on Windows XP.


Installers
==========

The One Click Installer requires that you have all the required component
installers in the same directory with it, and that they have expected
names. If Robot Framework or Python installer is missing, the
installation fails. If Jython installer does not exist, Jython is
simply not installed. Note that in order to install Jython, Java
version 1.4 or newer must be already installed. Minimum supported versions
are Robot Framework 2.0, Python 2.5 and Jython 2.2, but latest versions are
always recommended. These installers can be downloaded from the respective
project web sites. The expected patterns for installer names are
*robotframework-2.\*.exe* , *python-2.\*.msi*, and *jython_installer-2.\*.jar*.


Usage
=====

All you need to specify is the base directory where to install Python and
Jython. They are installed into the directories *Python* and
*Jython*, respectively, inside the given base directory. Robot
Framework itself is installed under the Python installation directory. Its
startup scripts can be found from *[PYTHON]\\Scripts* and code from
*[PYTHON]\\Lib\\site-packages*.

It is possible to run the One Click Installer from command line by giving the
installation directory as argument like
*RobotFrameworkOneClickInstaller.exe C:\\APPS\\*.


    **Note:**
        The specified base directory *MUST* exist, whereas Python and Jython
        directories inside it must not. It is also not recommended to
        use a path containing spaces. Good candidates include
        directories such as *C:\\* and *C:\\APPS\\*.

Screenshot
==========

.. figure:: https://bitbucket.org/robotframework/robottools/raw/master/oneclickinstaller/oneclickinstaller.png
   :width: 400
   :height: 250


.. _AutoIT: http://www.autoitscript.com/autoit3/
.. _Robot Framework: http://robotframework.org
.. _Python: http://www.python.org
.. _Jython: http://www.jython.org
