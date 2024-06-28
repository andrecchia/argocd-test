Simple argo CD test
- Install argocd in the kubernetes cluster
  ```shell
  kubectl create namespace argocd
  kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
  ```
- Expose
  ```shell
  kubectl port-forward svc/argocd-server -n argocd 8080:443
  ```
  then connect to localhost:8080 (password is contained in secret inside argocd namespace
