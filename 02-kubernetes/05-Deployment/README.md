 ```
   40  kubectl apply -f 01-helloworld.yaml 

   42  kubectl  get deploy 
   43  kubectl  get deploy,rs,pod
       kubectl expose deploy helloworld-deployment --type=NodePort
       kubctl get svc 
       kubctl get nodes -o wide 
       
       curl <nodeip>:<nodeport> : i.e curl 172.18.0.4:32742 

   41  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2
   44  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3
   45  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4
   46  cat helloworld.yaml 
   47  cat README.md 
   48  kubectl rollout history deploy helloworld-deployment
   49  kubectl rollout history deploy helloworld-deployment --revision=1
   50  kubectl rollout history deploy helloworld-deployment --revision=2
   51  kubectl rollout history deploy helloworld-deployment
   52  kubectl rollout undo deploy helloworld-deployment
   53  kubectl rollout history deploy helloworld-deployment
   54  kubectl rollout undo deploy helloworld-deployment
   55  kubectl rollout history deploy helloworld-deployment
   56  kubectl rollout undo deploy helloworld-deployment --to-revision=2
   57  kubectl rollout history deploy helloworld-deployment
   58  kubectl rollout undo deploy helloworld-deployment --to-revision=1
   59  kubectl rollout history deploy helloworld-deployment
   60  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record 
   61  kubectl rollout history deploy helloworld-deployment
   62  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record 
   63  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record 
   64  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web --record 
   65  kubectl rollout history deploy helloworld-deployment
```

