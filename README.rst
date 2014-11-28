shop
****

Django application for a shop

Install
=======

Virtual Environment
-------------------

::

  pyvenv-3.4 --without-pip venv-shop
  source venv-shop/bin/activate
  wget https://raw.githubusercontent.com/pypa/pip/master/contrib/get-pip.py
  python get-pip.py

  pip install -r requirements/local.txt

Testing
=======

::

  find . -name '*.pyc' -delete
  py.test -x

Usage
=====

::

  py.test -x && \
      touch temp.db && rm temp.db && \
      django-admin.py syncdb --noinput && \
      django-admin.py migrate --noinput && \
      django-admin.py demo_data_login && \
      django-admin.py runserver

Release
=======

https://www.pkimber.net/open/
