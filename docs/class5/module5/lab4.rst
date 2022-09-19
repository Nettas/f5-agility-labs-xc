Lab 4 - Publish to the Internet
===============================

#. Navigate the left-side menu to ``Manage`` > ``Load Balancers`` -> ``HTTP Load Balancers``, then click **Add HTTP Load Balancer**.

   .. image:: ../images/m-add-http.png
   
#. Enter a name for your HTTP Load Balancer in the **Metadata**.

   .. image:: ../images/m-http-name.png

#. In the **Basic Configuration** Section make the following changes:

    - **List of Domains**: Use your {namespace}.lab-app.f5demos.com
    - **Select Type of Load Balancer**: HTTPS with Automatic Certificate
    - **Select Type of Load Balancer**: Make sure this is checked

   .. image:: ../images/m-http-basic.png
      :width: 800px

#. In the **Default Origin Servers** Section click **Add item**.

   .. image:: ../images/m-add-origin-server.png
      :width: 800px

#. Select your **Origin Pool**, which was created earlier in this lab, and Click **Add Item**

   .. image:: ../images/m-select-origin-pool.png
      :width: 800px

#. In the Security Configuration section change the **Security Policies** to *Do Not Apply Service Policies* then click **Save and Exit**.

   .. image:: ../images/m-security-configuration.png
      :width: 800px
   
#. After a few moments you should see a screen like the following:

   .. image:: ../images/m-http-status.png
      :width: 800px

.. note::
  - Please wait for the VIRTUAL_HOST_READY and Valid certificate status before proceeding

Now we are ready to test!

Open a browser tab and navigate to the domain you entered. 

In the example below it is *flying-ox.lab-app.f5demos.com*

Success will render a page like the following:

.. image:: ../images/websrv_output.png
   :width: 800px

