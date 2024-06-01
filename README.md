

- Move to k8s directory
```bash
cd two-tier-flask-app/k8s
```
- Now, execute below commands one by one
```bash
kubectl apply -f twotier-deployment.yml
```
```bash
kubectl apply -f twotier-deployment-svc.yml
```
```bash
kubectl apply -f mysql-deployment.yml
```
```bash
kubectl apply -f mysql-deployment-svc.yml
```
```bash
kubectl apply -f persistent-volume.yml
```
```bash
kubectl apply -f persistent-volume-claim.yml
```

**Go to your worker node**
Cmds:
sudo docker ps
docker exec –it mysql /bin/bash
Inside cont:
mysql –u root –padmin
show databases;
use mydb;
create table messages( id int not null auto_increment primary key, message TEXT);
exit

