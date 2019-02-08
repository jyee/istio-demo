This directory contains all of the YAML for the demonstration

## Installing Istio

1. **Download Istio**

   ```
   curl -L https://git.io/getLatestIstio | sh -
   # cd to the istio version you downloaded
   cd istio-1.0.#
   export PATH=$PWD/bin:$PATH
   ```
   For more info, see https://istio.io/docs/setup/kubernetes/download-release/
1. **Install Istio**

   ```
   kubectl apply -f istio/install/kubernetes/istio-demo.yaml
   ```

   Note: if the install generates errors about "no matches for kind...", wait a second and re-run the command above. This usually happens when Kubernetes is not done fully setting up resources.
