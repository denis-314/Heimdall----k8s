Follow the below steps to deploy Heimdall App in Kubernetes using YAML files.

PREREQUISITES:

    l. Copy the above YAML file on a local directory
    2. Open communication on ports 30005 & 30006 on the Router (or other ports, but they need to be modified in transm_deployment.yml).

DEPLOYMENT STEPS:

    l. Create local directory in the OS for the persistent volume
        - mkdir /volume-files
    2. Create namespace
        - kubectl apply -f heimdall.yml
