# Kueue hops
Template crds:

```
helm template . --include-crds --show-only 'templates/crd/*.yaml' > crds/crds.yaml
```

And then add to webhook validate and mutate jobs:

```
objectSelector:
  matchLabels:
    app.kubernetes.io/managed-by: kueue
```
