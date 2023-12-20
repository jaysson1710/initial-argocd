
- [video-tutorial-initial](https://www.youtube.com/watch?v=MeU5_k9ssrs)
- [guia de instalacion yaml](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- [config repo & script de lanzamiento](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)

## commands

**screen 1**
```cmd
 2039  kubectl create namespace argocd
 2040  kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
 2041  kubectl get namespace argocd
 2042  k get svc -n argocd
 2046  k port-forward -n argocd svc/argocd-server 8080:443
```
** screen 2**
```cmd
 1996  kubectl get secret argocd-initial-admin-secret -n argocd -o yaml
 ## copiar el valor del secret y obtener el texto decodificado
 1997  echo TzAyTVlFQS1UWjZYYTNxQw== | base64 --decode
 2001  k get pods -n default
 2002  k get namespaces
 2003  nano app.yaml
 2004  k apply -f app.yaml 
 2001  k get pods -n default
 2002  k get namespaces
```