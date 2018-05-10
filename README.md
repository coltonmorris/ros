# Ros Experimentation


## Startup K8s
+ `bazel run //k8s:all.apply`


## Access Token for Kubernetes Dashboard
`gcloud config config-helper --format=json | jq .credential.access_token`

## Scale Down Clusters
Remember to scale down clusters when not actively developing :)
`gcloud container clusters resize $CLUSTER_NAME --size=0`


## TODO
+ Look into using minikube for local development and GCP for collaborative

### References
+ https://blog.zhaw.ch/icclab/challenges-with-running-ros-on-kubernetes/