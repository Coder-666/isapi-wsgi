**The new hosting location for isapi-wsgi is https://github.com/hexdump42/isapi-wsgi**

**Latest Release: 0.4.2 12 April 2010**

Description: An implementation of WSGI (PEP 333) for running as a ISAPI extension under IIS. WSGI is considered as important standard for the future of web deployed Python code. There are implementations for CGI, mod python, twisted, jython etc but at the start of development there was not one using ISAPI for IIS. The goal of this project is to provide one. It is dependant on Mark Hammond's Python [win32 isapi extension](http://sourceforge.net/projects/pywin32/).

Current status: The isapi\_wsgi adapter is considered stable. It has been used to deploy many wsgi compliant Python web applications and frameworks including [Django](http://www.djangoproject.com/), [TurboGears](http://turbogears.org/), [Mercurial](http://mercurial.selenic.com/) and [Trac](http://trac.edgewall.org/). It provides two handlers:

  * ISAPISimpleHandler - a new handler instance is created per request
  * ISAPIThreadPoolHandler - requests use the thread pool

You can checkout the latest version from the trunk (svn checkout http://isapi-wsgi.googlecode.com/svn/trunk/) or use one of the download packages.

The [examples](http://code.google.com/p/isapi-wsgi/source/browse/#svn/trunk/examples) directory shows a number of different use cases, including serving from IIS root.

Documentation: http://code.google.com/docreader/#p=isapi-wsgi&s=isapi-wsgi&t=isapi-wsgi

Mailing list: http://groups.google.com/group/isapi_wsgi-dev

CreditsAndThanks

Maintainers:

  * Mark Rees EMail: mark dot john dot rees at gmail dot com Blog: http://hex-dump.blogspot.com
  * Jason R. Coombs
  * Randy Syring