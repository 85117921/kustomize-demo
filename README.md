# kustomize-demo

refer to:
https://zhuanlan.zhihu.com/p/92153378
https://www.codercto.com/a/78064.html


## relative command 
kubectl kustomize  ./lion/overlays/dev/
kubectl kustomize  ./lion/overlays/dev/ | kubectl apply -f -

kubectl kustomize  ./lion/overlays/test/
kubectl kustomize  ./lion/overlays/test/ | kubectl apply -f -

kubectl kustomize  ./lion/overlays/prod/
kubectl kustomize  ./lion/overlays/prod/ | kubectl apply -f -

## check env
kubectl exec ${POD_NAME} -- env
