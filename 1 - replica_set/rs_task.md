# ReplicaSet Worksheet:

__Task 1, step 7: Enter the command you used for scaling the replica set:__
```
kubectl scale --replicas=3 -f replica_1.yml

```

__Task 1, step 9: What happened after applying another pod with matching selectors as the ReplicaSet?__
```
nginx-pod terminated as a new replica was added
 Type    Reason            Age    From                   Message
  ----    ------            ----   ----                   -------
  Normal  SuccessfulCreate  20m    replicaset-controller  Created pod: nginx-replica-c4lrx
  Normal  SuccessfulCreate  20m    replicaset-controller  Created pod: nginx-replica-g94gl
  Normal  SuccessfulCreate  6m33s  replicaset-controller  Created pod: nginx-replica-44ksg
  Normal  SuccessfulDelete  28s    replicaset-controller  Deleted pod: nginx-pod


```
