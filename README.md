# Ros Experimentation
Running ROS across [multiple machines](http://wiki.ros.org/ROS/Tutorials/MultipleMachines) in **Kubernetes**


## Startup K8s
+ `bazel run //k8s:all.apply`


## Access Token for Kubernetes Dashboard
`gcloud config config-helper --format=json | jq .credential.access_token`

## Scale Down Clusters
Remember to scale down or delete clusters when not actively developing :)   
+ `gcloud container clusters delete cluster-1 --zone us-central1-a`
+ `gcloud container clusters resize cluster-1 --zone us-central1-a --size=0`


## TODO
+ Experiment with scaling up and down `deployments`
+ Use a **Helm Chart** rather than rudimentary bazel aggregator
+ Look into using minikube for local development and GCP for collaborative

### References
+ https://blog.zhaw.ch/icclab/challenges-with-running-ros-on-kubernetes/
