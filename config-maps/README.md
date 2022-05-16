## Get Config Maps

```
k get cm
```

## Create a config map

### From the command line from literal

```
k create configmap <config_map> --from-literal=<key-value>

Example
k create configmap cm-options --from-literal=key=value
```

The values of the config map could be loaded from a file as well.

## Assign a config map to a pod

If you would like to load a config map into a pod, as environment variable, add this configuration to the pod template file

```
env:
    - name: <env_name>
      valueFrom:
        configMapKeyRef:
          name: <cm_name>
          key: <env_key>
```

Now apply the pod template


