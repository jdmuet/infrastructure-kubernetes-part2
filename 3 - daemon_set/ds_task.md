# DaemonSet Worksheet


__Task 4, step 5: Once you apply the DaemonSet, what happens and why?__

```
Creates Daemon set, but it is not available
NAME       DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR     AGE
nginx-ds   0         0         0       0            0           nodeType=health   48s


```

__Task 4, step 7: What happened when you labeled the node and why?__

```
once the label was added, the ds became active
NAME       DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR     AGE
nginx-ds   1         1         1       1            1           nodeType=health   2m42s

```
