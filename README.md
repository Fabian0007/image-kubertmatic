# image-kubertmatic
```
cd kubertmatic-dl
docker buildx build --platform linux/amd64 --load --no-cache -t kubermatic-dl-local .
docker tag kubermatic-dl-local fabiancr.azurecr.io/kubermatic-dl:v3
docker push fabiancr.azurecr.io/kubermatic-dl:v3
kubectl apply -f deployment.yaml
kubectl rollout restart deployment kubermatic-dl-deployment
kubectl get pods
cd ..
curl -X POST -F img=@plane-draw.jpeg http://20.253.208.216/predict
```
