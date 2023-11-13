# k8s-commands

### Power-shell
```
$env:KUBECONFIG = "${path_file_config}"
ls $ENV:KUBECONFIG


kubectl get services --all-namespaces
  [...]
kubectl describe services ${service_name}
  Name:              ${service}
  Namespace:         default
  Labels:            app.kubernetes.io/instance=${service}-${entorno}
  Annotations:       <none>
  Selector:          app=${service}
  Type:              ClusterIP
  IP Family Policy:  SingleStack
  IP Families:       IPv4
  IP:                10.0.X.2X8
  IPs:               10.0.X.2X8
  Port:              ${service}-http  YYYYY/TCP
  TargetPort:        http/TCP
  Endpoints:         10.100.100.2XX:YYYYY <-
  Session Affinity:  None
  Events:            <none>
kubectl get pods --all-namespaces
  [...]
kubectl get ingressRoutes --all-namespaces
  [...]
kubectl exec -it ${pod} -- /bin/bash
  [...]
kubectl logs ${pod}
  [...]
kubectl get deployment,middleware,pod,service,ingress ${pod} -o yaml
  [...]
kubectl get secret
  [...]
kubectl get secret
kubectl describe secret ${secret}
kubectl get secret ${secret} -o jsonpath='{.data}'
echo '$(kubectl get secret ${secret} -o jsonpath='{.data}')' | base64 --decode
```
