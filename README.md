# camunda-helm
Camunda managed via helm and K8s running on a Postgres database

## Credential setup
```
cat <<EOF | kubectl apply -f -
apiVersion: v1
kind: Secret
metadata:
  name: mysecret
type: Opaque
data:
  password: $(echo -n "camunda" | base64 -w0)
  username: $(echo -n "camunda" | base64 -w0)
EOF
```