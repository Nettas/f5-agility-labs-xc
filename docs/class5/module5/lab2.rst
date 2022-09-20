Lab 2 - Deploy a Web Server to the Managed K8s Cluster
======================================================

In this lab, we will learn the following:

•  Deploy a Managed K8s workload utilizing a containerized app from a public registry

•  Deploy to the Managed K8s site

#. Goto the following repo and either clone or copy and paste the deployment manifest from the below link into a directory on your local machine. 

    `Web-Server-for-XC-Managed-K8s-Training <https://github.com/Nettas/Web-Server-for-XC-Managed-K8s-Training/blob/main/AppStack-GCP/server-deployment/deployment.yaml/>`_

#. Utlizing the Global kubeconfig deploy the manifest.

   *Change to the directory where you saved the Deployment File and Apply it*
      `kubectl apply -f "filename.yaml"`
   
#. Validate all resources were deployed

   *From UI follow the same steps from Lab1 Excercise 2.  Just search for resources in your created namespace*

   *From CLI just append with your created namespace*

   *Namespace*

   .. code-block:: console

      $ kubectl get namespace

   *Deployment*

   .. code-block:: console

      $ kubectl get deployment -n "namespace"

   *Pods*

   .. code-block:: console

      $ kubectl get pods -n "namespace"

   *Service*

   .. code-block:: console

      $ kubectl get svc -n "namespace"

   *Get All resources for the Namespace you created*

   .. code-block:: console

      $ kubectl get all -n "namespace"

