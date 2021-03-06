Oncilla - Manual - Help File
============================

.. raw:: html

    <br/>

Table Of Content
=================

.. .tocTree

-  `Introduction`_
-  `Installation`_
-  `Usage`_

   -  `Prerequisites`_

      -  `Environment`_
      -  `Paths`_

   -  `Slicing`_
   -  `Execution`_

-  `Api`_
-  `Changes`_
-  `About`_

.. raw:: html

    <br/>

.. .introduction

_`Introduction`
===============

**Oncilla** is the documentation building helper package of `Oncilla <http://github.com/KelSolaar/Oncilla>`_, `Color <http://github.com/KelSolaar/Color>`_, `Manager <http://github.com/KelSolaar/Manager>`_, `Umbra <http://github.com/KelSolaar/Umbra>`_, `sIBL_GUI <http://github.com/KelSolaar/sIBL_GUI>`_ and `sIBL_Reporter <http://github.com/KelSolaar/sIBL_Reporter>`_.

With a single monolithic manual / help **reStructuredText** file used as input, an html manual file and the complete **Sphinx** documentation will be generated:

-  `Source manual reStructuredText file example <https://github.com/KelSolaar/sIBL_GUI/blob/master/docs/help/sIBL_GUI_Manual.rst>`_
-  `Output manual html file example <http://kelsolaar.hdrlabs.com/sIBL_GUI/Support/Documentation/Help/sIBL_GUI_Manual.html>`_
-  `Output sphinx documentation example <http://kelsolaar.hdrlabs.com/sIBL_GUI/Support/Documentation/Api/index.html>`_

.. raw:: html

    <br/>

.. .installation

_`Installation`
===============

The following dependencies are needed:

-  **Python 2.6.7** or **Python 2.7.3**: http://www.python.org/
-  **PyQt**: http://www.riverbankcomputing.co.uk/
-  **Tidy** http://tidy.sourceforge.net/

To install **Oncilla** from the `Python Package Index <http://pypi.python.org/pypi/Oncilla>`_ you can issue this command in a shell::

	pip install Oncilla

or this alternative command::

	easy_install Oncilla

You can also directly install from `Github <http://github.com/KelSolaar/Oncilla>`_ source repository::

	git clone git://github.com/KelSolaar/Oncilla.git
	cd Oncilla
	python setup.py install

.. raw:: html

    <br/>

.. .usage

_`Usage`
========

In order to build the project documentation, **Oncilla** needs some prerequisites.

_`Prerequisites`
----------------

_`Environment`
^^^^^^^^^^^^^^

You will need to have the following environment variables defined:

-  **ONCILLA_PROJECT_DIRECTORY**: Defines the project directory you want to build the manual and **Sphinx** documentation.
-  **ONCILLA_PROJECT_NAME**: Defines the name you want to use across the manual and **Sphinx** documentation files.
-  **ONCILLA_PROJECT_PACKAGES**: Defines the packages you want to build the **Sphinx** documentation.
-  **ONCILLA_PROJECT_SANITIZER**: Defines the optional **Sphinx** documentation sanitizing **Python** module.
-  **ONCILLA_PROJECT_EXCLUDED_MODULES**: Defines the optional excluded **Python** modules from **Sphinx** documentation.
-  **ONCILLA_PROJECT_MANUAL_CSS_FILE**: Defines the optional **css** stylesheet file used for the manual.

Example::

   export ONCILLA_PROJECT_DIRECTORY="/Users/kelsolaar/Documents/Development/sIBL_GUI"
   export ONCILLA_PROJECT_NAME="sIBL_GUI"
   export ONCILLA_PROJECT_PACKAGES="oncilla foundations manager umbra sibl_gui"
   export ONCILLA_PROJECT_SANITIZER="/Users/kelsolaar/Documents/Development/sIBL_GUI/utilities/sanitizer.py"
   export ONCILLA_PROJECT_EXCLUDED_MODULES="pyclbr tests 001_dummy 001_migrate_3-x-x_to_4-0-0 002_migrate_4-x-x_to_4-0-2 003_migrate_4-x-x_to_4-0-3 004_migrate_4-x-x_to_4-0-7 defaultScript"

_`Paths`
^^^^^^^^

**Oncilla** documentation is built with itself and is a good reference on how to structure your project documentation directories.

Assuming **$PROJECT_NAME** is the project name and **$PROJECT_DIRECTORY** the project root directory, the following paths need to be defined:

-  **$PROJECT_DIRECTORY/docs/help/$PROJECT_NAME_Manual.rst**: Source manual **reStructuredText** file.
-  **$PROJECT_DIRECTORY/docs/sphinx**: Standard **Sphinx** documentation root directory containing the **Makefile** and **source/conf.py** files.

_`Slicing`
----------

The **Sphinx** documentation pages are generated by slicing the source manual **reStructuredText** file using specific tags prepended by a dot ( **.** )::

   E.g.: .. .mySliceTag

For example, https://github.com/KelSolaar/Oncilla/blob/master/docs/help/Oncilla_Manual.rst file defines various tags like *.. .tocTree*, *.. .introduction*, *.. .installation*, etc..., and as a result the *tocTree.rst*, *introduction.rst*, *installation.rst* pages will be created and included into the **Sphinx** documentation.
 
_`Execution`
------------

Once the prerequisites have been defined, you can launch **Oncilla** using this shell command::

      Oncilla

.. raw:: html

    <br/>

.. .api

_`Api`
======

**Oncilla** Api documentation is available here: `Oncilla - Api <http://thomasmansencal.com/Sharing/Oncilla/Support/Documentation/Api/index.html>`_

.. raw:: html

    <br/>

.. .changes

_`Changes`
==========

**Oncilla** Changes file is available here: `Oncilla - Changes <http://thomasmansencal.com/Sharing/Oncilla/Changes/Changes.html>`_

.. raw:: html

    <br/>

.. .about

_`About`
========

| **Oncilla** by Thomas Mansencal - 2008 - 2014
| Copyright © 2008 - 2014 - Thomas Mansencal - `thomas.mansencal@gmail.com <mailto:thomas.mansencal@gmail.com>`_
| This software is released under terms of GNU GPL V3 license: http://www.gnu.org/licenses/
| http://www.thomasmansencal.com/