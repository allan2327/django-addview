Add views to Django app automatically - django-addview
======================================================

What it does?
-------------

Can't remember Class-Based-Views parameters? Are you tired of
reiterating the same mundane steps while adding a new view? Try
**django-addview**.

How it works?
-------------

Django-addview provides you with a simple ncurses based gui to add new
class-based or functional view.

-  Creates class declaration (fill needed parameters, select a model
   from the dropdown etc.)
-  Remembers all class-based attributes for you
-  Creates template (empty, or copied from existing one)
-  Adds entry to **urls.py**
-  Cares about all imports

Installation
------------

``pip install django_addview``

And add to settings.py:

::

    INSTALLED_APPS = (
        ...
        'django_addview',
    )

Usage
-----

``./manage.py addview app_name``

**Remember:** What you type inside app is what you get inside your code,
so if you want to have a string you have to quote it. For example:

::

    template_name       "test_app/my_view.html"

Configuration
-------------

Django-addview expects only one config variable. It's :
``ADDVIEW_GLOBAL_TEMPLATE_DIR = ...`` which points to directory where
you keep your project templates (It's good practice to keep templates
inside one directory per project unless you write reusable app).

Django-addview can create your views in two locations. One is
``ADDVIEW_GLOBAL_TEMPLATE_DIR`` and second is ``templates`` directory
inside your apps directory. You choose between them while adding view in
gui.

Example of configuration:

::

    SITE_ROOT = os.path.join(os.path.dirname(os.path.realpath(__file__)), '..')
    ADDVIEW_GLOBAL_TEMPLATE_DIR = os.path.join(SITE_ROOT, 'templates')

Screenshots
-----------

|screenshot 1| |screenshot 2| |screenshot 3| |screenshot 4|

.. |screenshot 1| image:: https://raw.github.com/yakxxx/django-addview/master/_screenshots/addview1.png?raw=true
.. |screenshot 2| image:: https://raw.github.com/yakxxx/django-addview/master/_screenshots/addview2.png?raw=true
.. |screenshot 3| image:: https://raw.github.com/yakxxx/django-addview/master/_screenshots/addview3.png?raw=true
.. |screenshot 4| image:: https://raw.github.com/yakxxx/django-addview/master/_screenshots/addview4.png?raw=true
