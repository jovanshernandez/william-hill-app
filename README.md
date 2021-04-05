# William Hill Docker App
### Build docker container from Dockerfile, then use kubectl to scale replicas to 3 running containers of app.

```
# Build docker image
docker build -t jshdevops/william-hill . 

# Run docker image detached
docker run -p 80:80 -d jshdevops/william-hill

# Check local host to verify output

# Deploy 3 replicas of container
kubectl apply -f wh-app-manifest.yaml
```