

## Generate the deployment definition without creating it

```
k create deployment nginx --image nginx --dry-run=client -oyaml > deployment.yml
```

## Apply deployment yml file

```
k apply -f deployment.yml
```

## Describe deployment

```
k describe deploy nginx
```

## Imperative way for scaling up the pods in the deployment

```
k scale deployment nginx --replicas 5
```

## Get deployment template definition

```
k get deploy nginx -oyaml > deploy-updated.yml
```
