Lab Optional - Use kubectl to view vk8s Output
==============================================

F5 Distributed Cloud App Stack provides the ability to manage your vk8s namespace via command line with kubectl 

In this lab, we will learn perform the following:

•  Review kubectl commands and see the output

Core concepts
-------------

   *Virtual kubernetes vK8s*
      `F5 Distributed Cloud Services support a Kubernetes compatible API for centralized orchestration of applications across a fleet of sites (customer sites or F5 Distributed Cloud Regional Edge). This API is “Kubernetes compatible” because not all Kubernetes APIs or resources are supported. However, for the API(s) that are supported, it is hundred percent compatible. We have implemented a distributed control plane within our global infrastructure to manage scheduling and scaling of applications across multiple (tens to hundreds of thousands of) sites, where each site in itself is also a managed physical K8s cluster.`

   *kubectl*
      `Standard upstream kubectl CLI tool can be used on the vK8s API URL or the downloaded kubeconfig file can be used to access the vK8s APIs.`

   For more core concepts, please review `F5 Distributed Cloud documentation <https://docs.cloud.f5.com/docs/ves-concepts/dist-app-mgmt>`_


kubectl commands
----------------

Run the following commands and view the outputs.  Why are there different outputs before and after increasing the replicas?

*View Nodes*

.. code-block:: console

   $ kubectl get nodes
   $ kubectl get nodes -o wide
   
*View pods*

.. code-block:: console
 
   $ kubectl get pods
   $ kubectl get pods -o wide
   $ kubectl describe pod <podname>
   
*View deployment and service*

.. code-block:: console

   $ kubectl get deployment agility
   $ kubectl get svc agility

*View all resources in your namespace*

.. code-block:: console

   $ kubectl get all

*View output of the pod in yaml format*

.. code-block:: console

   $ kubectl get pods <podname> -o yaml
 
*View output of the deployment in yaml format*

.. code-block:: console

   $ kubectl get deployment agility -o yaml

*View output of the service in yaml format*

.. code-block:: console

   $ kubectl get svc agility -o yaml
   
*Save the output of the deployment in yaml format*

.. code-block:: console

   $ kubectl get deployment -o yaml > agility.yaml

*View the saved yaml deployment*

.. code-block:: console

    $ cat agility.yaml

