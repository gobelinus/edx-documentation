.. _Installing Open edX Fullstack:

##############################################
Installing Open edX Fullstack
##############################################

This section describes how to install the Open edX full stack (fullstack).

.. contents::
   :local:
   :depth: 1

.. note::
  Before you install Open edX fullstack, make sure that you have met the
  :ref:`installation prerequisites<Installation Prerequisites>`.

.. note::
  Before beginning the installation, ensure that you have your local computer's
  administrator's password. The password is needed so that NFS can be set up to
  allow users to access code directories directly from your computer.

To install fullstack directly from the command line, follow these steps.

#. Ensure the ``nfsd`` client is running.

#. Create the ``fullstack`` directory and navigate to it in the command prompt.

   .. code-block:: bash

     mkdir fullstack
     cd fullstack

#. Download the fullstack Vagrant file.

   .. code-block:: bash

     curl -L https://raw.githubusercontent.com/edx/configuration/master/vagrant/release/fullstack/Vagrantfile > Vagrantfile

#. Install the Vagrant ``hostsupdater`` plugin.

   .. code-block:: bash

     vagrant plugin install vagrant-hostsupdater

#. Create the fullstack virtual machine.

   .. code-block:: bash

     vagrant up

   The first time you create the fullstack virtual machine, Vagrant downloads
   the base box, which has a file size of about 4GB. If you destroy and
   recreate the virtual machine, Vagrant re-uses the box it downloaded. See
   `Vagrant's documentation on boxes`_ for more information.

#. When prompted, enter the administrator password for your local computer.

.. include:: ../../../../links/links.rst
