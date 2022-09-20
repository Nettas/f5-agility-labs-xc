Lab 2 - Publish to the Internet
===============================

#. Navigate the left-side menu to ``Manage`` > ``Load Balancers`` > ``HTTP Load Balancers``, then click **Add HTTP Load Balancer**.

   .. image:: ../images/m-add-http.png
   
#. Enter a name for your HTTP Load Balancer in the **Metadata** section.

   .. image:: ../images/m-http-name.png

#. In the **Basic Configuration** Section make the following changes:

   - **List of Domains**: Use your {namespace}.lab-app.f5demos.com
   - **Select Type of Load Balancer**: HTTPS with Automatic Certificate
   - **Select Type of Load Balancer**: Make sure this is checked

   .. image:: ../images/m-http-basic.png

#. In the **Default Origin Servers** Section click **Add item**.

   .. image:: ../images/m-add-origin-server.png

#. Select your **Origin Pool**, which was created earlier in this lab, and Click **Add Item**

   .. image:: ../images/m-select-origin-pool.png

#. In the Security Configuration section change the **Security Policies** to *Do Not Apply Service Policies* then click **Save and Exit**.

   .. image:: ../images/m-security-configuration.png
   
#. After a few moments you should see a screen like the following:

   .. image:: ../images/m-http-status.png

.. note::
  - Please wait for the VIRTUAL_HOST_READY and Valid certificate status before proceeding

Open a browser tab and navigate to the domain you entered. 

In the example below it is *flying-ox.lab-app.f5demos.com*

Success will render a page like the following:

.. image:: ../images/m-http-status.png

Please note the country name. 

Refresh your browser a few times and notice what happens to the country name. 

