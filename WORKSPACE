workspace(name = "com_github_coltonmorris_ros")


### K8s
git_repository(
  name = "io_bazel_rules_docker",
  commit = "27c94dec66c3c9fdb478c33994471c5bfc15b6eb",
  remote = "https://github.com/bazelbuild/rules_docker.git",
)

load(
  "@io_bazel_rules_docker//container:container.bzl",
  container_repositories = "repositories",
)

container_repositories()

git_repository(
  name = "io_bazel_rules_k8s",
  commit = "4348f8e28b70cf3aff7ca8e008e8dc7ac49bad92",
  remote = "https://github.com/bazelbuild/rules_k8s.git",
)

load("@io_bazel_rules_k8s//k8s:k8s.bzl", "k8s_repositories", "k8s_defaults")

k8s_repositories()

k8s_defaults(
  name = "k8s_deploy",
  kind = "deployment",
  #   kubectl config current-context
  cluster = "gke_burningman-ros_us-central1-a_cluster-1",
  namespace = "default",
)
k8s_defaults(
  name = "k8s_service",
  kind = "service",
  #   kubectl config current-context
  cluster = "gke_burningman-ros_us-central1-a_cluster-1",
  namespace = "default",
)

