Lab 1 - Create Origin Pool
==========================

#. Navigate the left-side menu to ``Manage`` > ``Load Balancers``, then click ``Origin Pools``.

   .. image:: ../images/m-origin-pool.png
   
#. Click the **Add Origin Pool** button.

   .. image:: ../images/m3-add-origin-pools.png

#. On the New Origin Pool form:

   #. Enter a **Name** for your pool
   #. Replace the **Port** value of *443* with *3000*
   #. Select **Add Item** under **Origin Servers**

   .. image:: ../images/m-origin-pool-name.png

#. Complete the **Origin Server** section by make the following changes:

    - **Select Type of Origin Server**: K8s Service Name of Origin Server on given Sites
    - **Service Name**: workloadname.namespace (make a note to remember this in creation stage)
    - **Site or Virtual Site**: Virtual Site select shared/agility-k82-site
    - **Select Network on the site**: vK8s Networks on Site

   .. image:: ../images/m3-add-origin-server.png
 
#. Click on **Add Item** to return to the previous screen

#. Click the **Save and Exit** button to close the **Origin Pool** dialogue.

