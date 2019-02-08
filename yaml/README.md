This directory contains all of the YAML for the demonstration

## Installing Istio

1. **Download Istio**

   ```
   curl -L https://git.io/getLatestIstio | sh -
   cd istio-1.0.3
   export PATH=$PWD/bin:$PATH
   ```
   For more info, see https://istio.io/docs/setup/kubernetes/download-release/
1. **Install Istio**

   Istio has a number of custom resource definitions (CRDs) that first need to be defined.
   ```
   kubectl apply -f install/kubernetes/helm/istio/templates/crds.yaml
   ```
   Next, create the Istio namespace.
   ```
   kubectl create namespace istio-system
   ```
   Finally apply the Istio minimal installation from this project directory.
   ```
   kubectl apply -f istio/istio-minimal.yaml
   ```
   For more info, see https://istio.io/docs/setup/kubernetes/minimal-install/
