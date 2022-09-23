## Create Docker Image

```hcl
docker build -t flaskapp:latest .
```

## load image to kind cluster 

```hcl
kind load docker-image flaskapp:latest
```

## change the helm values in values.yml file according and deploy the helm chart

```hcl 
helm install <Release Name> <chart - name >/

helm install flaskapp chart/
```

## to uninstall

```hcl 
helm uninstall flaskapp
```

## access the content of web application

```hcl 
kubectl get nodes -o wide
```

- pick the ip address of node

```hcl 
kubectl get svc 
```

- pick the nodeport of service

## browse using url

```hcl
curl http://<ip>:<port>
```

## enable the ingress and modified the domain in values.yml  
