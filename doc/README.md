```shell
git clone git@github.com:athena-flow/kubeflow-manifests.git
sudo su
cd kubeflow-manifests
python install.py

kubectl get po -A
kubectl get pod -n kubeflow
kubectl logs katib-mysql-f6b75dd75-xj9bm -n kubeflow
kubectl exec -it katib-mysql-f6b75dd75-bmp7g bash

kubectl delete -f patch/auth.yaml
kubectl apply -f patch/auth.yaml

kubectl get po -A|grep kubeflow
sudo docker images|grep google

kubectl get pvc -A|grep kubeflow
kubectl describe pvc katib-mysql -n kubeflow
kubectl get storageclass

kubectl get sc
kubectl patch storageclass biocloud -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'

http://10.50.10.19:30000/
admin@example.com
password
```

```
Using a password on the command line interface can be insecure

No default Storage Class is set. Can't create new Disks for the new Notebook. Please use an Existing Disk.
k8s default Storage Class 
```

```
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: pvctest
  annotations:
    volume.beta.kubernetes.io/storage-class: "nfs-client"
spec:
  accessModes:
  - ReadWriteMany
  resources:
    requests:
      storage: 10Mi
```

