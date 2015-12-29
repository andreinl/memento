Appendix A
==========

LibrERP module numbers
----------------------

Module numbers has special semantic meaning. So "v.x.y.z" is version.model.code.xml.

version
    Defines the version of code formatting: 1 - No style, 2 - OpenERP 6.0 style, 3 - OpenERP 6.1/LibrERP style

model
    Increments when there are model changes

code
    Increments when code is changed

xml
    Increments when XML is changed

This way we know if application should be reloaded and module updated (like in case of model change), just reloaded (in case of code change), just updated (in case of xml change). This information is very useful for a production environment where not always you can tear down the application any time you want.
