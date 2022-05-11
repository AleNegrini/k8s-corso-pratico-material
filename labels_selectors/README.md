# Labels and Selectors

Let's create a few pods with different labels

```
k run nginx --image nginx --labels=app=v1
k run nginx2 --image nginx --labels=app=v1
k run nginx3 --image nginx --labels=app=v2
```

## Filters pods per label

```
k get po -l <label>

Example
k get po -l app=v1
```