# camunda-helm
Camunda managed via helm and K8s running on a Postgres database

## Credential setup
```
# Create files needed for rest of example.
echo -n 'camunda' > ./username.txt
echo -n 'camunda' > ./password.txt
kubectl create secret generic db-user-pass --from-file=./username.txt --from-file=./password.txt
```