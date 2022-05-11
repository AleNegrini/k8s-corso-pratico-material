# Namespaces

[Documentation](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)

## Get namespaces

Get the list of the current cluster namespaces

```
k get ns
```

## Get pods in a namespace

```
k get pods -n <namespace_name>
```

## Create a namespace

As did for pods, they can be created in two ways.

Imperatively:

```
k create ns mynamespace
```

Declaratively:

```
k create ns mynamespace -oyaml > myns.yml
k apply -f ns.yml
```


