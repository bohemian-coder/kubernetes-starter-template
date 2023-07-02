# kubernetes-starter-template
A single pod setup template for a mysql server, complete with persistent volume, p-volume claims and secrets

This setup includes the following:

1.) PersistentVolume mysql-pv, with capacity 250Mi

2.) PersistentVolumeClaim to request this PersistentVolume storage (request 250Mi of storage)

3.) Deployment named mysql-deployment, with mysql:latest image and the PersistentVolume Mounted at path /var/lib/mysql.

4.) NodePort type service named mysql with nodePort set to 30007.

5a.) A secret named mysql-root-pass with key pair value; key name is password and value is YUIidhb667

5b.) A secret named mysql-user-pass having some key pair values;
 key name is username and value is k_rin, second key is password and value is 8FmzjvFU6S.

5c.) A secret named mysql-db-url, key name is database and value is kdb3


### Run Command

kubectl apply -f `filename`