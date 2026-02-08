1. View Pods - kubectl get pods
2. Create/Run a Pod - kubectl run {desired pod name} --image={name of image from registry such as docker; a common one is nginx or httpd}
3. Allows you to edit yaml files - kubectl edit pod
4. Run a pod from a yaml file kubectl run {name} --image={image from repo} --dry-run=client -o yaml
5. to get yaml file templates/examples search within the webpage of the official kubernetes documentation
6. when pasting from the kube docs, first use/type ':set paste' and then paste what you copied. This will properly indent the code in the yaml file.
7. kubectl get pods -o wide gives you more info about a pod.
8. kubectl exect -it 'pod name' -- /bin/bash or /bin/sh
9. 