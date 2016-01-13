# gluster_for_cluster

These scripts are made for deploying **glusterfs** tiering on clusters. Consider 
having two types of nodes: cold and hot tier nodes.

There are several playbooks:

1. *install_gluster* installs glusterfs on nodes
2. *build_cold_tier* creates a cold tier cluster of cold_tier nodes from hosts.yml
3. *build_hot_tier* create a hot tier cluster of hot_tier nodes from hosts.yml
4. *configure_volumes* changes configuration of a volume
5. *detach_tier* detaches hot tier from cluster moving all data off the hot tier to cold tier

General use case is to run all playbooks in direct order as above.

Notice that these playbooks are assumed to run over bastion server with public IP.
This is done by using ssh.cfg that ansible uses. The bastion host address
is 83.149.198.48 and it is hardcoded in ssh.cfg. If your bastion IP is different
then you have to change it.