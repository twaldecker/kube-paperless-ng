# paperless-ngx on Kubernetes

- for single node deployments only
- no backup

deploy to kubernetes:

    kubectl create namespace paperless
    kubectl apply -n paperless -f kubernetes

add admin user:

    kubectl exec -it paperless-app-8458f9fddd-7pdvg -n paperless -- /bin/bash
    python3 manage.py createsuperuser

