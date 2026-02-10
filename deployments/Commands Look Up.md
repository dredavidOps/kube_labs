1. View Pods - kubectl get pods
2. Create/Run a Pod - kubectl run {desired pod name} --image={name of image from registry such as docker; a common one is nginx or httpd}
3. Allows you to edit yaml files - kubectl edit pod
4. Run a pod from a yaml file kubectl run {name} --image={image from repo} --dry-run=client -o yaml
5. to get yaml file templates/examples search within the webpage of the official kubernetes documentation
6. when pasting from the kube docs, first use/type ':set paste' and then paste what you copied. This will properly indent the code in the yaml file.
7. kubectl get pods -o wide gives you more info about a pod.
8. kubectl exect -it 'pod name' -- /bin/bash or /bin/sh
9. kubectl create deployment 'deployment name' --image='image name' --replicas='number of replicas' --dry-run=client -o yaml CREATES a deployment but does not run it yet. That command can also be redirected to a file to have the deployment in it.
10. kubectl apply -f 'deployment name' applies the deployment files and runs the pods
11. kubectl get replicasets.apps ---> this shows you the replicas available in the cluster.
12. You can apply an update to an image but to ensure users aren't disconnected kubernetes can take down part of the replicas, apply the update on them and then bring down the ones without the update so the ones with the update will be running and serve the update
13. Namespaces are logical groupings of resources within a single cluster so we can call it as vlan tagging and the resources here would be like ports on the switch. Policies can be assigned to specific namespaces to make your environment work efficiently and securely. 