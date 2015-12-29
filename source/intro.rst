Introduction
============

Preamble
--------
LibrERP is a modern Enterprise Management Software, released under the AGPL license, and featuring CRM, HR, Sales, Accounting, Manufacturing, Inventory, Project Management, ... It is based on OpenERP (Odoo) which in turn is based on OpenObject, a modular, scalable, and intuitive Rapid Application Development (RAD) framework written in Python 2.x.

OpenObject features a complete and modular toolbox for quickly building applications: integrated Object- Relationship Mapping (ORM) support, template-based Model-View-Controller (MVC) interfaces, a report generation system, automated internationalization, and much more.

Python is a high-level dynamic programming language, ideal for RAD, combining power with clear syntax, and a core kept small by design.


Useful links
------------
    - Main website: http://www.librerp.com/
    - Github repository: https://github.com/iw3hxn/LibrERP
    - Demo server: https://demo.librerp.com
    - Odoo (formerly OpenERP) Community Association: https://odoo-community.org
    - Odoo (formerly OpenERP, formerly TinyERP): https://www.odoo.com/
    - Learning Python: https://docs.python.org/2/


LibrERP Architecture
--------------------
LibrERP uses the well-known client-server paradigm, with different pieces of software acting as client and server depending on the desired configuration.Client software

LibrERP provides a web interface accessible using any modern browser. It can also be used with Android Client app.


Building an LibrERP module
--------------------------
To understand how modules works in LibrERP we will build a hypothetical *idea* module. The purpose of this module would be to help creative minds, who often come up with ideas that cannot be pursued immediately, and are too easily forgotten if not logged somewhere. It could be used to record these ideas, sort them and rate them.

.. note:: Modular development: LibrERP uses modules as feature containers, to foster maintainable and robust development. Modules provide feature isolation, an appropriate level of abstraction, and obvious MVC patterns.


Developer mode
--------------
You have much more information if you are working in "Developer mode". To activate it just click on **i** letter in the right upper corner and click "Activate the developer mode".

To be able to install new modules you should enable 'Extended View'. For *Administrator* user you should go to:

    * Settings -> Users -> Administrator -> Access Rights -> Usability and select **Extended View**
    * Reload the page
    * After reloading the page you will see new menu on the left: *Update Modules List*. After clicking on this menu your module will be in the list and you can install it.

.. note:: You should **reload** LibrERP if you change something in Python code, you should **reload** *and* **upgrade** module if you change columns, you should **upgrade** without reload if you changed XML.

