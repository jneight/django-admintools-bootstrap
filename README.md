django-admintools-bootstrap
===========================

Forked from https://bitbucket.org/salvator/django-admintools-bootstrap for custom needs and updates

Django Admin Bootstrap theme
============================

Twitter Bootstrap support for Django Admin. Requires django-admin-tools package.


TODO:

* Fix some bugs
* Add multi-dropdown support

Screenshots
-----------

Some model admin

.. image:: https://bitbucket.org/salvator/django-admintools-bootstrap/raw/929405e45d92/snapshot3.png


Usage
-----

Install package::

 $ pip install -e hg+https://bitbucket.org/salvator/django-admintools-bootstrap#egg=admintools_bootstrap

* Insert `admintools_bootstrap` to your INSTALLED_APPS before `admin_tools` and `django.contrib.admin` apps.
* Make sure you have static files application installed and configured. See https://docs.djangoproject.com/en/dev/ref/contrib/staticfiles/ for details.
* Enjoy.


Site name in navigation bar and title
-------------------------------------

admintools-bootstrap can use current site to display site name in admin interface.

To enable this feature, add `django.contrib.sites` to your `INSTALLED_APPS` list (if you have not yet).

Set site name and domain in `django.contrib.sites` admin.


Icons in menu items
-------------------

Bootstrap 2.0 has icons support. To attach icon to navigation menu item, add icon argument to constructor::

 items.AppList(
        _('Users'),
        models=('django.contrib.auth.*',),
        icon='icon-cog icon-white'
 )


Display fieldsets as tabs in changeform (0.0.2 version only)
------------------------------------------------------------

* user fieldsets attribute in your ModelAdmin class
* every fieldset should have name (first item in fieldset definition list)
* use change_form_template = 'admintools_bootstrap/tabbed_change_form.html' attribute in ModelAdmin

Settings
--------

Site link::

 ADMINTOOLS_BOOTSTRAP_SITE_LINK = '/'

If not False, display specified link to site in the top panel


Used software:
--------------

* http://addyosmani.github.com/jquery-ui-bootstrap/
* http://twitter.github.com/bootstrap/
* https://bitbucket.org/izi/django-admin-tools/
* http://www.crummy.com/software/BeautifulSoup/
* https://github.com/jezdez/django-appconf
* http://pypi.python.org/pypi/versiontools