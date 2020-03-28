# CSYE 7374 - Spring 2020

## Team Information

| Name | NEU ID | Email Address |
| --- | --- | --- |
|Jagmandeep Kaur | 001426439|kaur.j@husky.neu.edu |  | | |
|Mayank Barua| 001475187| barua.m@husky.neu.edu|
|Yogita Patil| 001435442|patil.yo@husky.neu.edu |
|Prajesh Jain| 001409343| Jain.pra@husky.neu.edu|

## Run Ansible Playbook

Open terminal and run the ```ansible-playbook``` command in the below format with parameters

To create the cluster run following

```bash
$ AWS_PROFILE=yous-aws-profile ansible-playbook setup-k8s-cluster.yaml --extra-vars "dns_zone=value state_store=value cluster_name=value profile=kops env=prod metricsServer_releaseName=k8smertricsserver clusterAutoscaler_releaseName=cluster-autoscaler"
```
To create the rds and vpc peering run following

```bash
$ ansible-playbook create-rds-and-peering.yaml --extra-vars "env=default/dev/prod cluster_name=value"
```

To delete the all the resources run following

```bash
$ ansible-playbook delete-k8s-cluster.yaml --extra-vars "profile=value env=default/dev/prod cluster_name=value state_store=value ssh_public_key=value"
```

