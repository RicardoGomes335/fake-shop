# Fake Shop Serverless Architecture

Este projeto implementa uma arquitetura serverless para uma loja online chamada **FakeShop** versionadas em Docker + Dockerhub + kubernetes, Pipelines CI/CD Github Actions + Cloudcraft e usando serviços cloud da AWS como, AWS EKS, AWS CLOUDFORMATION com o projeto hospedado no DockerHub. Esta arquitetura é escalável e fácil de gerenciar. Uso do Prometheus com monitoramento pelo Grafana.

<img src="/assets/diagramasaws/awsdiagram.png">

## Architecture Overview (Etapas para implementação)

1. **UserGroup Access IAM**: Criação do grupo de usuario com o respectivos Polices na AWS.
2. **User Access IAM**: Criação do usuário IAM ( não root) e adicionado ao UserGroup.
3. **Create IAM Role Kubernetes Cluster**: Criação de uma Role IAM do cluster Kubernetes.
4. **NewRole AWS Service EKS**: Vincular cluster EKS ao ECS com as respectivas Policies.
5. **CloudFormation**: Criar a rede pelo CloudFormation com upload de um template.
6. **Create EKS Cluster**: Criar cluster EKS pelo painel AWS.
7. **Install AWS CLI**: Intalar o AWS CLI (Usei o Mac e o Linux).
8. **Add EKS Node Group**: Adicionar o grupo de nodes do EKS selecionando as redes public/private.
9. **Deploy CLICommand**: Fazer o deploy pelo terminal.

## AWS CLI CONFIG

<img src="/assets/aws-cli/aws-cli.png">

## Obtendo a URL do Projeto ( Cluster EKS)

<img src="/assets/aws-cli/aws-url.png">

## Repositório hospedado no DockerHub

<img src="/assets/dockerhub-screenshot/dockerhub.png">

## Monitoramento de Custos da arquitetura com CLOUDCRAFT

<img src="/assets/cloudcraft-screenshot/Dashboard1.png">

## Implementação CI/CD com Github Actions

<img src="/assets/github-actions-screenshot/CI:CD-GithubActions.png">

## Screenshot da aplicação

<img src="/assets/screenshotapp/V3app.png">

## URL da Aplicação

<http://a427491f3261b4534a4f21ac735f0f5b-83007396.us-east-1.elb.amazonaws.com/>

## Prometheus config

<img src="/assets/prometheus-config-cli/CLI.png">

## Grafana Kubernetes dashboard

<img src="/assets/grafana/kubernetes.png">

## Grafana Prometheus dashboard

<img src="/assets/grafana/prometheus.png">
