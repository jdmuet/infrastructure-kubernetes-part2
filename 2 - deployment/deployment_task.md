# Deployment Worksheet

__Task 2, step 6: After completing step 5 of task 2, what do you notice about the `ReplicaSet` - what is this used for?__
hint: use ` kubectcl get rs --show-labels`

```
It's given a pod-template-hash number. This is provides the ability to move between versions 
nginx-deployment-7cbbccf745   2         2         2       16m   app.kubernetes.io/version=1.0,app_name=nginx,env=dev,pod-template-hash=7cbbccf745

```

__Task 2, step 7: what command did you use to scale the deployment?__

```
kubectl scale --replicas=3 -f deployment_1.yml

```

__Task 3, step 2: Why are there two replica sets but only one deployment?__

```
AME                               READY   UP-TO-DATE   AVAILABLE   AGE   LABELS
deployment.apps/nginx-deployment   3/3     3            3           47m   app.kubernetes.io/version=2.0

NAME                                          DESIRED   CURRENT   READY   AGE    LABELS
replicaset.apps/nginx-deployment-7cbbccf745   3         3         3       47m    app.kubernetes.io/version=1.0,app_name=nginx,env=dev,pod-template-hash=7cbbccf745
replicaset.apps/nginx-replica                 3         3         3       101m   <none>
[dmuetzel1@WFIL204 manifests]$ 

```

__Task 3, step 6: What command did you use to roll back the deployment?__

```
kubectl rollout undo deployment/nginx-deployment  --to-revision=1
```
