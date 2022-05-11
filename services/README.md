
## Deployment

### Expose an existing deployment

Define in an imperative way a `Cluster IP service`.
The exposed port corresponds to the node port: `8080`.

```
k expose deployment mysimpleapp --port 8080 --target_port 8080
```

### Get services

```
k get svc
```



