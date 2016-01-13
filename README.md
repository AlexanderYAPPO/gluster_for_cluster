# gluster_for_cluster

This scripts are made for deploying glusterfs tiering on clusters. It's considered
to having two types of nodes: cold and hot tier nodes. The name of the gluster
cluster will be gv0.

There are several playbooks:

1. install_gluster installs glusterfs on nodes
2. build_cold_tier creates a cold tier cluster for cold_tier nodes from hosts.yml
3. build_hot_tier create a hot tier cluster for hot_tier nodes from hosts.yml
4. configure_volumes changes configuration of a volume
5. detach_tier detaches hot tier from tier cluster

General use case is to run all playbooks in direct order

Notice that this playbooks are assumed to run over bastion server with public IP.
This is done by changed ssh.cfg that ansible uses. The bastion host address
is 83.149.198.48 and it is hardcoded in ssh.cfg. If your bastion IP is different
then you have to change it.