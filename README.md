# camunda-helm
Camunda managed via helm and K8s running on a Postgres database

## Postgres Database build
```
cd postgres
docker build -t "camunda-ee-postgresql:latest" .
```

## Credential setup
```
cat <<EOF | kubectl apply -f -
apiVersion: v1
kind: Secret
metadata:
  name: camunda-database-credentials
type: Opaque
data:
  password: $(echo -n "camunda" | base64 -w0)
  username: $(echo -n "camunda" | base64 -w0)
EOF
```