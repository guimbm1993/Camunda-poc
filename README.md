# Arquivo .bpmn para ser aberto no modeler

# Instruções para criação da fila
docker run --rm -it -p 4566:4566 -p 4510-4559:4510-4559 localstack/localstack

awslocal sqs create-queue --queue-name localstack-queue

awslocal sqs list-queues

awslocal sqs receive-message --queue-url http://sqs.us-east-1.localhost.localstack.cloud:4566/000000000000/localstack-queue
