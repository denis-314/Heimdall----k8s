Follow the below steps to deploy Heimdall App in Kubernetes using YAML files.

PREREQUISITES:

    l. Copy the above YAML file on a local directory
    2. Open communication on ports 30005 & 30006 on the Router (or other ports, but they need to be modified in transm_deployment.yml).

DEPLOYMENT STEPS:

    l. Create local directory in the OS for the persistent volume
        - mkdir /volume-files
    2. Create namespace
        - kubectl apply -f heimdall.yml


---

- For the version of Heimdall exposed with Ingress service, I didn't find a way to add a subpath (http://domain/heimdall) to the custom domain (http://domain) configured with environment variables.
- Environment variables can be defined in the deployment manifest file, but for some reason, they are not passed to the .env file inside the container (/conf/www/.env), so they need to be manually modified, either directly inside the container, but preferably in the persistend volume.


- Option 1: with "pathType: Prefix"
- Left side image: Ingress rule for Heimdall
- Right side image: .env config file in the persistent volume

![image](https://github.com/denis-314/Heimdall----k8s/assets/112620749/4317324a-1ed7-4f76-accd-8007a592b0de)

- Option 2: with "pathType: Prefix"
- Left side image: Ingress rule for Heimdall
- Right side image: .env config file in the persistent volume

![image](https://github.com/denis-314/Heimdall----k8s/assets/112620749/e2d0a962-7cc4-4938-b946-d2fc1f95586a)
