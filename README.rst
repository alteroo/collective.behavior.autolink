****************************
collective.behavior.autolink
****************************

.. contents:: Table of Contents

Life, the Universe, and Everything
==================================

A behavior for Dexterity-based content types to add automatically created links from the content title.

Use cases
^^^^^^^^^

Suppose you are running Encyclopedia.com, a reference information portal.

Sometimes you have new page written about some subject in the portal, and you need to review all related pages
and add some links to the new page when it is relevant.

This package allows you to automatize this link creation with the new page, creating new links where the title of the
new page appears in the old pages.

Mostly Harmless
===============

.. image:: http://img.shields.io/pypi/v/collective.behavior.autolink.svg
   :target: https://pypi.python.org/pypi/collective.behavior.autolink

.. image:: https://img.shields.io/travis/collective/collective.behavior.autolink/master.svg
    :target: http://travis-ci.org/collective/collective.behavior.autolink

.. image:: https://img.shields.io/coveralls/collective/collective.behavior.autolink/master.svg
    :target: https://coveralls.io/r/collective/collective.behavior.autolink

Got an idea? Found a bug? Let us know by `opening a support <https://github.com/collective/collective.behavior.autolink/issues>`_.

Don't Panic
===========

Installation
^^^^^^^^^^^^

To enable this package in a buildout-based installation:

#. Edit your buildout.cfg and add add the following to it:

.. code-block:: ini

    [buildout]
    ...
    eggs =
        collective.behavior.autolink

After updating the configuration you need to run ''bin/buildout'', which will take care of updating your system.

Go to the 'Site Setup' page in a Plone site and click on the 'Add-ons' link.

Check the box next to ``collective.behavior.autolink`` and click the 'Activate' button.

How does it work
^^^^^^^^^^^^^^^^

This package adds a transformer to the transform chain to add new links into Plone.

The transformer looks for titles of content types with the behavior enabled in the text and transform the text into a link to the content type.

These transforms are applied to anonymous users only.

Enabling collective.behavior.autolink
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* In 'Site Setup', select the Dexterity Content Types configlet
* Select your content type
* Go to Behaviors tab and select collective.behavior.autolink
