Add helm bitnami repo: `helm repo add bitnami https://charts.bitnami.com/bitnami`

DB install: `helm install db -f helm-postgres/values.yml bitnami/postgresql`

Apply secrets: `kubectl apply -f api-config.yml`

Run migrations: `kubectl apply -f initdb.yml`

Run app: `kubectl apply -f deployment.yml -f service.yml -f ingress.yml`
