## Kubernetes Manifests
Service -> Deployment (ModSec) -> App (Ghost Blog)

## Helm Chart
TBD

NOTE: This pull request is going to be brought into the Ubuntu-Apache v2.9 folder very shortly: https://github.com/CRS-support/modsecurity-docker/pull/23/files#diff-3254677a7917c6c01f55212f86c57fbf

First Things:
1. Do you have a GCP account of some sort?
2. Do you have the GCP SDK installed? https://cloud.google.com/sdk/install

GCP Managed Base Images:
1. Looks like you have to build the Google Managed Image locally first instead of Docker just knowing to grab it based on your FROM statement
2. `gcloud auth configure-docker && docker pull marketplace.gcr.io/google/debian9:latest`
3. Users will need a GCP account of some kind, but then again Docker Hub also requires accounts too

Linking With Github:
1. You can mirror the whole repository to Google Source Repositories. 
2. OR you can install Google Cloud Build Github App. This is in Alpha/Beta and is more difficult though.
3. See here: https://cloud.google.com/cloud-build/docs/run-builds-with-github-checks


NOTE: https://github.com/organizations/AstraAspera/settings/installations