# gluster_for_cluster

This scripts are made for deploying glusterfs tiering on clusters. It's considered
to having two types of nodes: cold and hot tier nodes.

There are several playbooks:

1. install_gluster installs glusterfs on nodes
2. build_cold_tier creates a cold tier cluster for cold_tier nodes from hosts.yml
3. build_hot_tier create a hot tier cluster for hot_tier nodes from hosts.yml