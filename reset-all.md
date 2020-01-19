1 - Stop

docker container stop $(docker container ls -aq)

2 - Remove

docker container rm $(docker container ls -aq)

3 - Images Prune

docker image prune -a

4 - Volume Prune

docker volume prune

5 - Reset Kubernetes

kubeadm reset

6 - Clean All Durectories

rm -rf /etc/ceph \
       /etc/cni \
       /etc/kubernetes \
       /opt/cni \
       /opt/rke \
       /run/secrets/kubernetes.io \
       /run/calico \
       /run/flannel \
       /var/lib/calico \
       /var/lib/etcd \
       /var/lib/cni \
       /var/lib/kubelet \
       /var/lib/rancher/rke/log \
       /var/log/containers \
       /var/log/pods \
       /var/run/calico





docker rm -f $(docker ps -qa)
docker rmi -f $(docker images -q)
docker volume rm $(docker volume ls -q)
