# kustomize-demo

refer to:
https://zhuanlan.zhihu.com/p/92153378
https://www.codercto.com/a/78064.html

## init a base layer
$ kubectl apply -k ./lion/base/
service/lion-88 created
deployment.apps/lion-88 created
## if you directly use apply -f , it will encounter error
kubectl apply -f ./lion/base 
### and also why can not auto-delete server/lion-88 ?

## relative command 
kubectl kustomize  ./lion/overlays/dev/
kubectl kustomize  ./lion/overlays/dev/ | kubectl apply -f -

kubectl kustomize  ./lion/overlays/test/
kubectl kustomize  ./lion/overlays/test/ | kubectl apply -f -

kubectl kustomize  ./lion/overlays/prod/
kubectl kustomize  ./lion/overlays/prod/ | kubectl apply -f -

## check env
kubectl exec ${POD_NAME} -- env
