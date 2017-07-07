# chart-prometheus
K2 supported prometheus chart

**Note: this chart was forked from: https://github.com/kubernetes/charts/tree/master/stable/prometheus**

Detailed readme found [here](./prometheus/README.md)


## Sample installation
Depending on your kubernetes version of your cluster and whether you implement RBAC or ABAC:

- k8s version < 1.5

    ```
    helm install --namespace kube-monitoring --name prometheus --set server.service.type=NodePort
    ```

- k8s version > 1.6 with rbac

    ```
    helm install --namespace kube-monitoring --name prometheus --set kubernetes.rbac=true --set server.service.type=NodePort
    ```
    
    you can change the type to be the `LoadBalancer`, `ClusterIp (default)` or `NodePort` 

