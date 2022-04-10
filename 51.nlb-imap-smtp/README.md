# Commands

```bash
helm repo add eks https://aws.github.io/eks-charts
kubectl apply -k "github.com/aws/eks-charts/stable/aws-load-balancer-controller//crds?ref=master"
helm install aws-load-balancer-controller eks/aws-load-balancer-controller -n kube-system --set clusterName=${CLUSTER_NAME} --set serviceAccount.create=false --set serviceAccount.name=aws-load-balancer
```

## Connect via NLB

```bash
telnet k8s-inmem-smtp-a71231e463-0cb7c5c6c8533a4a.elb.ap-northeast-1.amazonaws.com 8001
Trying 52.193.81.96...
Connected to k8s-inmem-smtp-a71231e463-0cb7c5c6c8533a4a.elb.ap-northeast-1.amazonaws.com.
Escape character is '^]'.
220 Apache JAMES awesome SMTP Server
```
