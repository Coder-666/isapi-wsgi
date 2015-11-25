# ISAPI\_WSGI 0.4.2 #

This document relates the current version of the isapi\_wsgi handler released in April 2010.

## Dependencies ##

  * Python 2.3+
  * Python win32 extensions that include the isapi package
  * wsgiref library from http://cvs.eby-sarna.com/wsgiref/ (included in Python 2.5+)
  * A windows webserver that supports ISAPI (isapi\_wsgi has been tested on IIS 5.1, 6.0 and 7.0)
  * **IIS 7.x must have IIS 6.0 Management Compatability installed.**
  * If IIS is 64bit but installed python is 32bit, enable 32bit applications in app pool. See http://code.google.com/p/isapi-wsgi/issues/detail?id=10

## Installation ##

Python 2.3 or better is required.

Get isapi-wsgi using any of these methods:

  * from [PyPi](http://pypi.python.org/pypi/isapi_wsgi/)
  * easy\_install isapi\_wsgi
  * Download the archive or windows installer from [here](http://code.google.com/p/isapi-wsgi/downloads/list)

If you downloaded the archive, to install, just unpack it, go to the directory containing 'setup.py', and run:

python setup.py install

isapi\_wsgi.py will be installed in the 'site-packages' directory of your Python installation. (Unless directed elsewhere; see the "Installing Python Modules" section of the Python manuals for details on customizing installation locations, etc.).

(Note: for the Win32 installer release, just run the .exe file.)

To help with deployment you may find [ISAPIWSGIHelper](http://pypi.python.org/pypi/ISAPIWSGIHelper/) useful. ISAPIWSGIHelper is a small command line script and some helper utilities to help bootstrap deployment of WSGI applications using isapi-wsgi with Microsoft IIS.

## Testing ##

As a user with admin privileges run the command:

```
python isapi_wsgi.py install
```

to create a simple ISAPI test extension in an IIS virtual directory called isapi-wsgi-test. This can be accessed from a webbrowser using the url:

http://localhost/isapi-wsgi-test/

If there are no errors and a simple web page is displayed, then the installation of isap\_wsgi was successful.

To remove the test virtual directory, run the command:

```
python isapi_wsgi.py remove
```