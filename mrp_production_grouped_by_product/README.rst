=============================
Production Grouped By Product
=============================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:fc6bfd0803818e81b30ef12e570b837a625a243513c3f167f8c5471ee7d7d825
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fmanufacture-lightgray.png?logo=github
    :target: https://github.com/OCA/manufacture/tree/15.0/mrp_production_grouped_by_product
    :alt: OCA/manufacture
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/manufacture-15-0/manufacture-15-0-mrp_production_grouped_by_product
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/manufacture&target_branch=15.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

When you have several sales orders with make to order (MTO) products that
require to be manufactured, you end up with one manufacturing order for each of
these sales orders, which is very bad for the management.

With this module, each time an MTO manufacturing order is required to be
created, it first checks that there's no other existing order not yet started
for the same product and bill of materials inside the specied time frame , and
if there's one, then the quantity of that order is increased instead of
creating a new one.

**Table of contents**

.. contents::
   :local:

Configuration
=============

To configure the time frame for grouping manufacturing order:

#. Go to *Inventory > Configuration > Warehouse Management > Operation Types*
#. Locate the manufacturing type you are using (default one is called
   "Manufacturing").
#. Open it and change these 2 values:

   * MO grouping max. hour (UTC): The maximum hour (between 0 and 23) for
     considering new manufacturing orders inside the same interval period, and
     thus being grouped on the same MO. IMPORTANT: The hour should be expressed
     in UTC.
   * MO grouping interval (days): The number of days for grouping together on
     the same manufacturing order.

   Example: If you leave the default values 19 and 1, all the planned orders
   between 19:00:01 of the previous day and 20:00:00 of the target date will
   be grouped together.

Known issues / Roadmap
======================

* Add a check in the product form for excluding it from being grouped.

Changelog
=========

15.0.1.0.0 (2022-09-12)
~~~~~~~~~~~~~~~~~~~~~~~

* [MIG] Migration to v15.

14.0.1.0.0 (2021-11-16)
~~~~~~~~~~~~~~~~~~~~~~~

* [MIG] Migration to v14.

13.0.1.0.0 (2020-01-09)
~~~~~~~~~~~~~~~~~~~~~~~

* [MIG] Migration to v13.

12.0.1.0.0 (2019-04-17)
~~~~~~~~~~~~~~~~~~~~~~~

* [MIG] Migration to v12:

11.0.2.0.1 (2018-07-02)
~~~~~~~~~~~~~~~~~~~~~~~

* [FIX] fix test in mrp_production_grouped_by_product

11.0.2.0.0 (2018-06-04)
~~~~~~~~~~~~~~~~~~~~~~~

* [IMP] mrp_production_grouped_by_product: Time frames

11.0.1.0.1 (2018-05-11)
~~~~~~~~~~~~~~~~~~~~~~~

* [IMP] mrp_production_grouped_by_company: Context evaluation on mrp.production + tests

11.0.1.0.0 (2018-05-11)
~~~~~~~~~~~~~~~~~~~~~~~

* Start of the history.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/manufacture/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/manufacture/issues/new?body=module:%20mrp_production_grouped_by_product%0Aversion:%2015.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Tecnativa

Contributors
~~~~~~~~~~~~

* `Tecnativa <https://www.tecnativa.com>`__

  * David Vidal
  * Pedro M. Baeza

* `Ecosoft <https://ecosoft.co.th/>`__:

  * Pimolnat Suntian <pimolnats@ecosoft.co.th>

* `ForgeFlow <https://www.forgeflow.com/>`__:

  * Lois Rilo <lois.rilo@forgeflow.com>

* `Punt Sistemes <https://www.puntsistemes.com/>`__:

  * Salva Benlloch <sbenlloch@puntsistemes.es>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/manufacture <https://github.com/OCA/manufacture/tree/15.0/mrp_production_grouped_by_product>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
