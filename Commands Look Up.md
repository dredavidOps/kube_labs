1. View Pods - kubectl get pods
2. Create/Run a Pod - kubectl run {desired pod name} --image={name of image from registry such as docker; a common one is nginx or httpd}
3. Allows you to edit yaml files - kubectl edit pod
4. Run a pod from a yaml file kubectl run {name} --image={image from repo} --dry-run=client -o yaml
5. 