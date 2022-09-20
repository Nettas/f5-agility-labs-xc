Lab 1 - Review vK8s Cluster and Deploy vK8s Workload
====================================================

In this lab, we will learn the following:

•  Review the previously-created Virtual K8s cluster
•  Configure a vK8s workload utilizing a containerized app from a private registry
•  Deploy a vK8s workload within a vK8s site
•  Advertise a vK8s workload within a cluster via custom HTTP port

Core concepts
-------------

   *Workload*
      `Workload is used to configure and deploy a workload in Virtual Kubernetes. A workload may be part of an application. Workload encapsulates all the operational characteristics of Kubernetes workload, storage, and network objects (deployments, statefulsets, jobs, persistent volume claims, configmaps, secrets, and services) configuration, as well as configuration related to where the workload is deployed and how it is advertised using L7 or L4 load balancers. A workload can be one of simple service, service, stateful service or job. Services are long running workloads like web servers, databases, etc. and jobs are run to completion workloads. Services and jobs can be deployed on regional edges or customer sites. Services can be exposed in-cluster or on Internet by L7 or L4 load balancer or on sites using an advertise policy.`

   *Service*
      `A service with one or more containers with configurable number of replicas that can be deployed on a selection of Regional Edge sites or customer sites and advertised within the cluster where is it deployed, on the Internet, or on other sites using TCP or HTTP or HTTPS load balancer.`

   *Deploy*
      `Since Kubernetes is becoming the de-facto industry standard for orchestrating applications, F5® Distributed Cloud has chosen to implement its control plane with a Kubernetes compatible API for orchestration while delivering additional capabilities of managing and securing multiple clusters across distributed locations. This makes it seamless to integrate with third party tools like Spinnaker for CI/CD, etc. For packaging of microservices, we prefer Docker images, which have become another de-facto approach.`

   For more core concepts, please review `F5 Distributed Cloud documentation <https://docs.cloud.f5.com/docs/ves-concepts/dist-app-mgmt>`_

Review Virtual K8s Site
-----------------------

#. Access ``Distributed Apps`` in the console.

   .. image:: ../images/1access_distributed_apps_service_menu.png
      :width: 800px

#. Select ``Applications`` > ``Virtual K8s``, and select the cluster from the list.

   .. image:: ../images/2access_applications_vk8s.png
      :width: 800px

#. Select ``Dashboard`` on the vK8s dashboard.

   .. image:: ../images/3review_vk8s_dashboard_sites.png
      :width: 800px

Configure vK8s Workload Container
---------------------------------

#. Select ``Workloads`` > **Add vK8s workload**

   .. image:: ../images/4add_vk8s_workload.png
      :width: 800px

#. Complete the **Metadata** section by providing a **Name** and **Description**, then select **Service** from the **Type of Workload** list. Next, select **Configure** within the **Service** sub-section.

   .. image:: ../images/5workload_metadata_and_service.png
      :width: 800px

#. Select |add-item| within the **Containers** section.

   .. image:: ../images/6add_container.png
      :width: 800px

#. Complete the **Container Configuration** section by providing a **Name** and details for which **Image to Use**.

   - **Image Name**: coleman.azurecr.io/f5xcdemoapp
   - **Container Registry**: Private Registry
   - **Private Registry**: shared/azure-registry

   .. image:: ../images/7container_config.png
      :width: 800px

Configure vK8s Workload Deployment Options
------------------------------------------

#. Within the **Deploy Options** section, set **Where to Deploy the Workload** to *Customer Virtual Sites*, then **Configure** within the **Customer Virtual Sites** section.

   .. image:: ../images/8deploy_options.png
      :width: 800px

#. Select your vK8s site name from **List of Virtual Sites to Deploy**, then |apply|

   .. image:: ../images/9select_customer_site.png
      :width: 800px

Configure vK8s Workload Advertisement Options
---------------------------------------------

#. Within the **Advertise Options** section, set **Options to Advertise the Workload** to *Advertise in Cluster*, then select **Configure** within the **Advertise in Cluster** section.

   .. image:: ../images/10select_advertise_options.png
      :width: 800px

#. Within the **Select Port to Advertise** section, set **Select Port to Advertise** to *Port*, click |apply| and then |save-and-exit|

   - **Port**: 3000
   - **Application Protocol**: HTTP

   .. image:: ../images/11set_advertise_port.png
      :width: 800px

#. The workload has been added with 3 sites and 3 pods.

   .. image:: ../images/12verify_3_workload_sites_pods.png
      :width: 800px

.. |add-item| image:: ../images/add-item.png
   :height: 24px

.. |apply| image:: ../images/apply.png
   :height: 24px

.. |save-and-exit| image:: ../images/save-and-exit.png
   :height: 24px
