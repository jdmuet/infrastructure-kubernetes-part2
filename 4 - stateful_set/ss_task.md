# StatefulSet Worksheet

__Task 5, step 3: Describe what happened and what you noticed about the pods and the volumes for them.__

```
enter answer here
```

__Task 5, step 4: Did anything change? Why or why not?__

Nothing changed because the UpdateStrategy was set to OnDelete, so the pod would need to be deleted before the next version was started.
```

__Task 5, step 6: What happened and why?__

```
New version was started for one of the pods
```

__Task 5, step 9: What happens this time?__

```
New version was started for all the pods
```

__Task 5, step 11: Repeat step 10. Was everything deleted? Why or why not?__

```
Only the pods were deleted, the persistantvolumeclaim was stil there. 
```
