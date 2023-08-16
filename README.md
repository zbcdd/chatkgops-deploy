# chatops-deploy

```
kubectl apply -f ./opentelemetry/cert-manager.yaml
(or kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.12.0/cert-manager.yaml)

kubectl apply -f ./opentelemetry/opentelemetry-operator.yaml
(or kubectl apply -f https://github.com/open-telemetry/opentelemetry-operator/releases/latest/download/opentelemetry-operator.yaml)

kubectl apply -f ./opentelemetry/instrumentation.yaml -n obs
kubectl apply -f ./opentelemetry/openTelemetryCollector.yaml -n obs


helm install tempo ./tempo -n obs
helm install loki ./loki-stack -n obs
helm install prometheus ./kube-prometheus-stack -n obs

cd ts-deploy
make deploy

```
