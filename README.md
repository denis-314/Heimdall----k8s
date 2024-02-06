Follow the below steps to deploy Heimdall App in Kubernetes using YAML files.

PREREQUISITES:

    l. Copy the above YAML file on a local directory
    2. Open communication on ports 30005 & 30006 on the Router (or other ports, but they need to be modified in transm_deployment.yml).
    3. Create the "/volume-files" local directory used as persistent volume

DEPLOYMENT STEPS:

    l. Create namespace
        - kubectl apply -f heimdall.yml
