# Pods

[Documentation] (https://kubernetes.io/docs/concepts/workloads/pods/)

## List all pods

### List all pods in all namespaces

```
k get pods --all-namespaces
```


### List all pods in the default namespace

```
k get pods
```

### List all pods in a specific namespace

```
k get pods --namespace <namespace_name>
```

## Create a new pod 

A pod can be created in two ways:

* imperativily
* declaratively

If not esplicitly stated, the pods are created in the default namespace

### Imperative way

```
k run <label> --image <image> 
```

Example
```
k run nginx --image nginx
```

### Declarative way

Using a `yml` template file, just apply it:

```
k apply -f <pod_template_path>
```

Example
```
k apply -f ./nginx-pod.yml
```

## Describe pod

```
k describe pod <pod_name>
```

Example
```
k describe po nginx
```

## Get the pod template definition

```
k run <pod_name> --image <image_name> --dry-run=client -oyaml
```

Example 
```
k run nginx_template --image nginx --dry-run=client -oyaml
```

After this command, the pod template is generated

You can save the template into a `.yml` file by running:

```
k run nginx_template --image nginx --dry-run=client -oyaml > pod-generated-template.yml
```

## Connect to the pod

```
k exec -it nginx -- sh
```



