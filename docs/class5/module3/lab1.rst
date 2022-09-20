Lab 1 - Create Origin Pool
==========================

#. Navigate the left-side menu to ``Manage`` > ``Load Balancers``, then click ``Origin Pools``.

   .. image:: ../images/m-origin-pool.png
      :width: 800px
   
#. Click the **Add Origin Pool** button.

   .. image:: ../images/m3-add-origin-pools.png
      :width: 800px

#. On the New Origin Pool form:

   * Enter a **Name** for your pool
   * Replace the **Port** value of *443* with *3000*
   * Select |add-item| under ``Origin Servers``

   .. image:: ../images/m-origin-pool-name.png
      :width: 800px

#. Complete the **Origin Server** section by make the following changes and click |add-item|

   * **Select Type of Origin Server**: K8s Service Name of Origin Server on given Sites
   * **Service Name**: workloadname.namespace (make a note to remember this in creation stage)
   * **Site or Virtual Site**: Virtual Site select shared/agility-k82-site
   * **Select Network on the site**: vK8s Networks on Site

   .. image:: ../images/m3-add-origin-server.png
      :width: 800px
 
#. Click |save-and-exit| near the **Origin Pool** dialogue.

.. |save-and-exit| image:: ../images/save-and-exit.png
   :height: 24px

.. |add-item| image:: ../images/add-item.png
   :height: 24px

.. |apply| image:: ../images/apply.png
   :height: 24px
