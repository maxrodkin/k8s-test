Part 2 - Elaboration on tasks
- What problems did you encounter? How did you solve them?

I chooze RKE "Installing Rancher on a Single Node Using Docker" case according to https://rancher.com/docs/rancher/v2.x/en/installation/other-installation-methods/single-node-docker/
The provisioning stucks at step:
This cluster is currently Provisioning; areas that interact directly with it will not be available until the API is ready.
[etcd] Successfully started etcd plane.. Checking etcd cluster health
[etcd] Failed to bring up Etcd Plane: etcd cluster is unhealthy: hosts [172.31.23.220] failed to report healthy. Check etcd container logs on each host for more information
The reason in etcd log:
2020-05-15 15:49:50.164470 I | embed: rejected connection from "172.31.23.220:37722" (error "tls: failed to verify client's certificate: x509: certificate signed by unknown authority (possibly because of \"crypto/rsa: verification error\" while trying to verify candidate authority certificate \"kube-ca\")", ServerName "")

And i didn`t resolve last etcd error. Tryed play with network settings and custom CA cert according to 
https://rancher.com/docs/rancher/v2.x/en/installation/requirements/#networking-requirements

So, thank you for very interesting training, will continue to solve task by myself for educational purposes.
 



