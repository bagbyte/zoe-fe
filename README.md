Deploying the Angular FrontEnd
==============================

Overview
--------
* This repository contains the zoe angular frontend for [zoe](https://github.com/DistributedSystemsGroup/zoe) main repository.

Installation
------------
Installation can be done in two different ways. Both require installation of a few packages, which are listed in ``package.json``. All dependencies can be installed simply by running ``npm install`` from the root folder.

1. Development Server

 * The first way to install the frontend is to install a local development server; this server will automatically reload when source files are changed. This can be done by the following two steps:

   * Run ``ng serve``
   * Navigate to ``http://localhost:4200/``

2. Proxy Server

 * The second way to install zoe can be done using a proxy with zoe:
 * Run ``ng build -prod --output-path=prod``

   * This will create all the build files in the ``/prod`` directory. These files need to be copied to the frontend server setup in the proxy configuration.
   * Note that in order to change the ``<base href="/">`` within the ``index.html`` file, it is possible to add the following to the ``ng build`` command: ``--base-href x`` where x is the new href value.
 * The output can be put behind a Nginx or Apache proxy.

Read more
---------
More information for deploying the angular project can be found in its documentation at ``DETAILS.md``.
