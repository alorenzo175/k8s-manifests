This repository contains Kubernetes templates to run a proof of concept
SolarForecastArbiter on AWS and access at
https://aws-dashboard.solarforecastarbiter.org.


An AWS EKS cluster, EFS filesystem, and a MySQL RDS instance are required.
Furthermore, the
[kubernetes-external-secrets](https://github.com/godaddy/kubernetes-external-secrets)
CRD and [cert-manager](https://cert-manager.io/) CRD with a self-signed issuer
must be installed in the EKS cluster. The manifests may be applied using
``kubectl apply -k .``


Currently, only GFS forecasts and NOAA SURFRAD data are fetched to avoid
unecessary cost. There is also one
[reference report](https://aws-dashboard.solarforecastarbiter.org/reports/6f5a7cf6-0433-11eb-bf0b-4ea881a1165b)
that is periodically regenerated with new observations/forecasts.
