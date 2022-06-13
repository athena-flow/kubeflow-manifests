```shell
git clone git@github.com:athena-flow/kubeflow-manifests.git
sudo su
cd kubeflow-manifests
python install.py

kubectl get po -A

kubectl get po -A|grep kubeflow
```
