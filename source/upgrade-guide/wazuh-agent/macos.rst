
.. Copyright (C) 2015, Wazuh, Inc.
.. meta::
  :description: Check out how to upgrade the Wazuh agent to the latest available version remotely, using the agent_upgrade tool or the Wazuh API, or locally.


Ugrading Wazuh agents on macOS systems
======================================

Follow these steps to upgrade Wazuh agents locally on macOS systems. If you want to perform a remote upgrade, check the :doc:`Remote agent upgrade </user-manual/agents/remote-upgrading/upgrading-agent>` section to learn more. 

.. note:: To perform the agent upgrade, administrator privileges are required.

#. Download the latest `macOS installer <https://packages.wazuh.com/|WAZUH_CURRENT_MAJOR_OSX|/macos/wazuh-agent-|WAZUH_CURRENT_OSX|-|WAZUH_REVISION_OSX|.pkg>`_. 

#. Run the macOS installer by using the command line interface (CLI) or the graphical user interface (GUI).

   .. tabs::
    
      .. group-tab:: CLI

         To upgrade the Wazuh agent by using the command line, run the installer:

         .. code-block:: console

            # installer -pkg wazuh-agent-|WAZUH_CURRENT_OSX|-|WAZUH_REVISION_OSX|.pkg -target /


      .. group-tab:: GUI

         Using the GUI will perform a simple upgrade. Double click on the downloaded file and follow the wizard. If you are not sure how to answer some of the prompts, simply use the default answers.

         .. image:: /images/installation/macos.png
            :align: center
            :scale: 50 %


.. note::
   :class: not-long

   When upgrading agents from versions earlier than 4.x, make sure that the communication protocol is compatible. Up to that point, UDP was the default protocol and it was switched to TCP for later versions. Edit the agent configuration file ``ossec.conf`` to update the :ref:`protocol <server_protocol>` or make sure that your Wazuh manager accepts :ref:`both protocols<manager_protocol>`. 

  