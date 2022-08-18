**Create resources**  

cd infra
aws cloudformation deploy --template-file infra.yml --stack-name observability-demo --parameter-overrides file://parameters-dev.json

**Delete resources**  

aws cloudformation delete-stack --stack-name observability-demo

**Start grafana & prometheus**  
docker compose -f ObservabilityDemo/infra/docker-compose-observability.yml up
