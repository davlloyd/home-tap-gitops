# Create Supplychain Basic Function

- create structure 
    tanzu supplychain init --group supplychains.tanzu.vmware.com --description "Source to Run Supplychain"

- Create Supplyc chain
    tanzu supplychain generate \                                                                  
    --kind WebApp \
    --description "Build and deploy an application from Git" \
    --component source-git-provider-1.0.0 \
    --component buildpack-build-1.0.0 \
    --component conventions-1.0.0 \
    --component app-config-web-1.0.0 \
    --component carvel-package-1.0.0 \
    --component deployer-1.0.0

- Apply to cluster
    NAMESPACE=custom-supply-chains make install


k get ch