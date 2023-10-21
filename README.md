### Deploy model_example_bbb via `DREAM cli`, `kubectl cli` or `docker` 

__via DREAM cli__ 
Simple way to deploy to k8s


```
dream models deploy model_example_bbb v3
```


__via kubectl directly__
Direct way to deploy to k8s


```
git clone --branch v3 --single-branch git@github.com:dreamutherland/model_example_bbb.git
kubectl create namespace serve-model-model-example-bbb
kubectl create -f mlflow-serving.yaml
kubectl expose deployment model_example_bbb-deployment --port [PORT] --type="LoadBalancer"
```


__via docker (local)__
Local way to quickly test the image


```
docker run -d -p PORT:PORT jleighsutherland/model_example_bbb:v3
```


### Test "model_example_bbb" by executing `./infer.sh` 

__via infer.sh__ 


```
./infer.sh
```

