Structure
=========

Typical module structure
------------------------
Each module is contained in its own directory. Standard modules are in the server/bin/addons directory in the server installation.

LibrERP modules are in a separate directory, that should be declared in the configuration file of LibrERP (passed to the server with the -c option) using the addons_path option.

.. note:: It can be a good idea to keep your own modules in a separate directory.


Every module should contain at least two files:
    - **__init__.py**: special Python file which transforms a simple directory in Python module.
    - **__openerp__.py**: module definitions including description, version, dependencies etc.

A module may contain any of the following elements:
    - **models**: declared as Python classes extending the *orm.Model* OpenObject class, the persistence of these resources is completely managed by OpenObject;
    - **views**: declared in XML visual data rapresentation;
    - **data**: XML/CSV files with meta-data (views and workflows declaration), configuration data (modules parametrization) and demo data (optional but recommended for testing, e.g. sample ideas);
    - **wizards**: stateful interactive forms used to assist users, often available as contextual actions on resources;
    - **reports**: report templates, to be merged with any kind of business data, and generate HTML, ODT or PDF reports. LibrERP can use various tecnologies to create a report, including OpenERP standard RML (XML format), MAKO or OpenOffice report templates;
    - **security**: access control definitions stored in CSV files;
    - **i18n**: module translations;
    - **static**: static data, like images, CSS, JavaScript;
    - **demo**: demo data;
    - **tests**: unit tests;


*idea* structure::

    addons/
        |- idea/                       # The module directory
            |- data/
                |- idea_data.xml               # Population data
            |- demo/
                |- idea_demo.xml               # Demo data
            |- models/
                |- idea.py                     # Python classes, the module's objects
            |- tests/                      # Unit testing data
            |- i18n/                       # Translation files
            |- report/                     # Report definitions
            |- security/                   # Declaration of groups and access rights
                |- ir.model.access.csv         # Who can access table and what is permitted (read, write, create, delete)
            |- views/
                |- idea_view.xml               # Views (forms,lists), menus and actions
            |- wizard/                     # Wizards definitions
            |- __init__.py                 # Python package initialization  (required)
            |- __openerp__.py              # module declaration (required)
            |- idea_workflow.xml           # Workflow definitions




