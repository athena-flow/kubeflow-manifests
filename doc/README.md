```shell
git clone git@github.com:athena-flow/kubeflow-manifests.git
sudo su
cd kubeflow-manifests
python install.py

kubectl get po -A

kubectl get po -A|grep kubeflow
sudo docker images|grep google

kubectl get pvc -A|grep kubeflow
kubectl describe pvc katib-mysql -n kubeflow
kubectl get storageclass
```

```
Using a password on the command line interface can be insecure
```
