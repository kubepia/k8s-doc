# k8s 관련 명령어 및 환경 변수

## etcd

### etctctl 실행

```shell
kubectl exec -itn openshift-etcd [pod-name] -c etcd-member sh
export ETCDCTL_API=3 ETCDCTL_CACERT=/etc/ssl/etcd/ca.crt ETCDCTL_CERT=$(find /etc/ssl/ -name *peer*crt) ETCDCTL_KEY=$(find /etc/ssl/ -name *peer*key)
etcdctl member list
```
