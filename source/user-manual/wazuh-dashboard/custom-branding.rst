.. Copyright (C) 2015, Wazuh, Inc.

.. meta::
   :description: Discover how to customize the appearance of your Wazuh dashboard and PDF reports.

How to set up custom branding
=============================
        
The Wazuh dashboard white-labeling feature allows you to replace the following elements with custom ones.

-  Logos in the Wazuh dashboard.
-  Logo, header, and footer in PDF reports.

Custom logos in the Wazuh dashboard 
-----------------------------------

To use your own logos in the Wazuh dashboard, click on the `App main logo` and go to **Settings** > **Configuration**. Under the **Custom branding** section, set up the following properties:

-  ``customization.logo.app``. This property sets the `App main logo` image. It has a size limit of 1 MB. It replaces the logo image in the Wazuh main menu located top left. Recommended size: 300 pixels width, 70 pixels height. See #1 in the image below.

-  ``customization.logo.healthcheck``. This property sets the `Health check logo` image. It has a size limit of 1 MB. It replaces the logo on top of the check list displayed during the health check routine. Recommended size: 300 pixels width, 70 pixels height. See #2 in the image below.

-  ``customization.logo.sidebar``. This property sets the `Navigation drawer logo` image. It has a size limit of 1 MB. It replaces the left navigation menu logo image. Recommended size: 80 pixels width, 80 pixels height. See #3 in the image below.

.. thumbnail:: /images/kibana-app/features/white-labeling/custom-branding-settings.jpg
   :align: center
   :width: 80%

Once you are done setting your custom logo images, you can find them saved in ``/usr/share/wazuh-dashboard/plugins/wazuh/public/assets/custom/images/``.

Custom branding of the PDF reports
----------------------------------

To customize the PDF reports, click on the `App main logo` and go to **Settings** > **Configuration**. Under the **Custom branding** section, set up the following properties:

-  ``customization.reports.logo``. This property sets the `PDF reports logo` image. It has a size limit of 1 MB. It's printed in the top left corner of the PDF reports. Recommended size: 190 pixels width, 40 pixels height. See #1 in the image below.

-  ``customization.reports.footer``. This property sets the `Reports footer` text block. It has a size limit of 2 lines of 50 characters each. It's printed in the bottom left corner of the PDF reports. See #2 in the image below.

-  ``customization.reports.header``. This property sets the `Reports header` text block. It has a size limit of 3 lines of 40 characters each. It's printed in the top right corner of the PDF reports. See #3 in the image below.

.. thumbnail:: /images/kibana-app/features/white-labeling/custom-pdf-report.jpg
   :title: Custom PDF report
   :align: center
   :width: 80%

Configuration
-------------

The following settings correspond to the custom branding feature. Edit them using the user interface as explained above. 

**customization.enabled**

    Enables and disables custom branding of the Wazuh dashboard and PDF reports.

    +--------------------+-----------------------+
    | Allowed values     |  true, false          |
    +--------------------+-----------------------+
    | Default value      |  true                 |
    +--------------------+-----------------------+

**customization.logo.app**

    This is the image to be used as the logo in the main menu of the app.
    It is saved as ``/usr/share/wazuh-dashboard/plugins/wazuh/public/assets/custom/images/customization.logo.app.<format>``.

    +--------------------+----------------------------+
    | Allowed format     | jpeg, jpg, png, svg        |
    +--------------------+----------------------------+
    | Default value      | ''                         |
    +--------------------+----------------------------+
    | Maximum file size  | 1 MB                       |
    +--------------------+----------------------------+

**customization.logo.healthcheck**

    This is the image to be used as the health check logo.
    It is saved as ``/usr/share/wazuh-dashboard/plugins/wazuh/public/assets/custom/images/customization.logo.healthcheck.<format>``.

    +--------------------+----------------------------+
    | Allowed format     | jpeg, jpg, png, svg        |
    +--------------------+----------------------------+
    | Default value      | ''                         |
    +--------------------+----------------------------+
    | Maximum file size  | 1 MB                       |
    +--------------------+----------------------------+

**customization.logo.sidebar**

    This is the image to be used as the sidebar logo.
    It is saved as ``/usr/share/wazuh-dashboard/plugins/wazuh/public/assets/custom/images/customization.logo.sidebar.<format>``.

    +--------------------+----------------------------+
    | Allowed format     | jpeg, jpg, png, svg        |
    +--------------------+----------------------------+
    | Default value      | ''                         |
    +--------------------+----------------------------+
    | Maximum file size  | 1 MB                       |
    +--------------------+----------------------------+

**customization.logo.reports**

    This is the image to be used as logo in the PDF reports generated by the app.
    It is saved as ``/usr/share/wazuh-dashboard/plugins/wazuh/public/assets/custom/images/customization.logo.reports.<format>``.

    +--------------------+----------------------------+
    | Allowed format     | jpeg, jpg, png             |
    +--------------------+----------------------------+
    | Default value      | ''                         |
    +--------------------+----------------------------+
    | Maximum file size  | 1 MB                       |
    +--------------------+----------------------------+

**customization.reports.header**

    Header of the PDF reports. To use an empty header, type a space " " in the field. If the field is empty, it uses the default header.

    +--------------------+------------------------+
    | Allowed characters | Printable characters   |
    +--------------------+------------------------+
    | Default value      | ''                     |
    +--------------------+------------------------+
    | Value limit        | 3 lines of             |
    |                    | 40 characters each     |
    +--------------------+------------------------+

**customization.reports.footer**

 	Footer of the PDF reports. To use an empty footer, type a space " " in the field. If the field is empty, it uses the default footer.

    +--------------------+----------------------+
    | Allowed characters | Printable characters |
    +--------------------+----------------------+
    | Default value      | ''                   |
    +--------------------+----------------------+
    | Value limit        | 2 lines of           |
    |                    | 50 characters each   |
    +--------------------+----------------------+
