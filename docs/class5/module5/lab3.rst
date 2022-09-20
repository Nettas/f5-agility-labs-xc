Lab 3 - Create Origin Pool
==========================

#. Navigate the left-side menu to ``Manage`` > ``Load Balancers``, then click ``Origin Pools``.

   .. image:: ../images/m-origin-pool.png
      :width: 800px
   
#. Click the **Add Origin Pool** button.

   .. image:: ../images/m3-add-origin-pools.png
      :width: 800px

#. On the New Origin Pool form:

   * Enter a **Name** for your pool (use the namespace you created i.e. s-iannetta)
   * Replace the **Port** value of *443* with *80*
   * Select **Add Item** under **Origin Servers**

   .. image:: ../images/m-origin-pool-name.png
      :width: 800px

#. Complete the **Origin Server** section by make the following changes, and click |add-item| and |save-and-exit| to close the **Origin Pool** dialogue.

   * **Select Type of Origin Server**: K8s Service Name of Origin Server on given Sites
   * **Service Name**: workloadname.namespace (make a note to remember this in creation stage)
   * **Site or Virtual Site**: Site select system/agility-vpc-site-one, two, or three depending on which site you selected for managedk8s
   * **Select Network on the site**: Outside Network

   .. image:: ../images/origin-pool.png
      :width: 800px
 
.. |save-and-exit| image:: ../images/save-and-exit.png
   :height: 24px

.. |add-item| image:: ../images/add-item.png
   :height: 24px

.. |apply| image:: ../images/apply.png
   :height: 24px
