# 🚀 Automação DevOps com Terraform, Docker e CI/CD

## 📖 Visão Geral

Este projeto demonstra um fluxo completo de DevOps, utilizando Infraestrutura como Código, containerização e automação de CI/CD.

A infraestrutura é provisionada na AWS utilizando Terraform, a aplicação é containerizada com Docker, e um pipeline de CI/CD com GitHub Actions realiza automaticamente o build da imagem e o envio para o DockerHub.

A aplicação é executada dentro de um container Docker utilizando Nginx em uma instância EC2 da AWS.

---

## 🏗 Arquitetura do Projeto

Repositório GitHub  
↓  
GitHub Actions (Pipeline CI/CD)  
↓  
Build da Imagem Docker  
↓  
DockerHub (Registro de Imagens)  
↓  
AWS EC2  
↓  
Container Docker com Nginx

---

## 🧰 Tecnologias Utilizadas

- Terraform
- AWS EC2
- Docker
- DockerHub
- GitHub
- GitHub Actions
- Nginx
- Linux

---

## 📂 Estrutura do Projeto

terraform-devops-infrastructure

app/  
  index.html  

docker/  
  Dockerfile  

terraform/  
  main.tf  
  provider.tf  
  variables.tf  
  outputs.tf  

.github/workflows/  
  deploy.yml  

---

## ⚙️ Pipeline CI/CD

O pipeline de CI/CD é executado automaticamente sempre que ocorre um push na branch main.

Etapas da automação:

1. Checkout do repositório  
2. Build da imagem Docker  
3. Login no DockerHub  
4. Envio da imagem para o DockerHub  

Esse processo garante que a imagem da aplicação esteja sempre atualizada.

---

## 🐳 Container Docker

Construir a imagem Docker:

docker build -t devops-app -f docker/Dockerfile .

Executar o container:

docker run -d -p 80:80 devops-app

Após executar o container, a aplicação ficará acessível através do IP público da instância EC2.

---

## ☁️ Provisionamento da Infraestrutura

A infraestrutura é criada utilizando Terraform.

Principais comandos utilizados:

terraform init  
terraform plan  
terraform apply  

Recursos criados:

- Instância EC2 na AWS
- Security Groups
- Configuração de rede

O Terraform permite que toda a infraestrutura seja recriada automaticamente.

---

## 🔄 Conceitos DevOps Demonstrados

Este projeto demonstra na prática:

- Infraestrutura como Código (IaC)
- Containerização
- CI/CD
- Automação de infraestrutura em nuvem
- Boas práticas de DevOps

---

## 📈 Possíveis Melhorias Futuras

Melhorias que podem evoluir este projeto:

- Deploy automático na EC2
- Orquestração com Kubernetes
- Monitoramento com Prometheus e Grafana
- Balanceamento de carga com AWS Load Balancer

---

## ‍💻 Autora
 Rayane Santana

Projeto desenvolvido para estudo prático de **Engenharia DevOps e Cloud Computing
