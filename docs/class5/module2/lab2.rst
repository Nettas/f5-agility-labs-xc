Lab 2 - Scale vK8s Deployment
=============================

In this lab, we will learn the following:

•  Review the Virtual K8s Cluster Dashboard

•  Modify Virtual K8s Deployment to Scale Replicas

Core concepts
------------

   *Pods in vK8s*
      `The core concept in application management on Kubernetes is a Pod. Pod is the basic and smallest execution unit that can be created, deployed, and managed in Kubernetes. A Pod consumes compute, memory, and storage resources and needs a network identity. A Pod contains single or multiple containers but it is a single instance of an application in Kubernetes.`

   *Service*
      `A service with one or more containers with configurable number of replicas that can be deployed on a selection of Regional Edge sites or customer sites and advertised within the cluster where is it deployed, on the Internet, or on other sites using TCP or HTTP or HTTPS load balancer.`

   For more core concepts, please review `F5 Distributed Cloud documentation <https://docs.cloud.f5.com/docs/ves-concepts/dist-app-mgmt>`_

Virtual K8s Cluster Dashboard
-----------------------------

#. Select ``Applications`` > ``Virtual K8s`` > ``Dashboard``. You should see one pod per site.

   .. image:: ../images/13validate_vK8s_dashboard.png
      :width: 600pt

#. Select ``Deployments``, then select the menu under **Actions** for your deployment, then ``Edit``

   .. image:: ../images/14edit_deployment.png
      :width: 600pt

#. Ensure **Edit** mode is enabled, expand the **spec** section, and modify **replicas** from *1* to *3* and select **Save**

   .. image:: ../images/15modify_deployment_spec.png
      :width: 600pt

Review Scaled vK8s Deployment
-----------------------------

#. It may take a few moments, but on the vK8s cluster dashboard, number of **Running Pods** should increase to 9. Upon refreshing the list, you may notice the number of **Sites with Error** gradually decrease as **Running Pods** increases.

   .. image:: ../images/16review_scaled_deployment.png
      :width: 600pt

