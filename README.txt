11/23/2012

Cucumber Bootstrap includes
- Twitter-bootstrap
- Slickgrid
- flot.js
- jquery
- underscore.js
- backbone.js
- backbone.js example todos.js
- Python dependency stack
  * MySQL
  * Django
  * Tornado
  * eventlet
  * jinja2 templating


Installing on Mac OSX 10.7.5

1)
Download and install Python 2.7.3 64-bit dmg from python.org

2)
Set PATH variable to include
/Library/Frameworks/Python.framework/Versions/2.7/bin

3)
Download and install using python above, setuptools-0.6c11 from
pypi.python.org (python.org dmg does not come with easy_install)


4)
Download and install using python above, pip-1.2.1 from
pypi.python.org (python.org dmg does not come with pip)

5)
Download and install MySQL community edition 5.5.19-osx10.6-x86_64.

6)
Install virtualenv using pip

7)
Configure virtualenv with
% virtualenv env

8) Activate virtualenv with
% . env/bin/activate

9)
Install all dependencies with pip and requirements.txt
% pip install -r requirements.txt

10)
Fix MySQL-python dylib to MySQL install with
% install_name_tool -change libmysqlclient.18.dylib \
/usr/local/mysql/lib/libmysqlclient.18.dylib \
$PWD/env/lib/python2.7/site-packages/_mysql.so


