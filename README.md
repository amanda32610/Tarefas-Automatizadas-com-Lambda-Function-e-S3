# Executando Tarefas Automatizadas com Lambda Function e S3

## 📌 Descrição do Projeto
Este projeto foi realizado como parte do desafio da DIO para praticar **automatização de tarefas com AWS Lambda e S3** usando **CloudFormation**.  
O objetivo foi criar uma Stack que provisiona automaticamente:

- Um bucket S3  
- Uma função Lambda  
- Permissões IAM para que a Lambda acesse o bucket  

A função Lambda é acionada automaticamente quando **um objeto é criado no bucket S3**, registrando o evento em logs.

---

## 🛠️ Tecnologias Utilizadas
- **AWS CloudFormation** – Criação da Stack automatizada  
- **AWS Lambda** – Função executando automaticamente  
- **AWS S3** – Armazenamento de arquivos que aciona a Lambda  
- **AWS IAM** – Permissões para Lambda acessar S3 e CloudWatch Logs  

---

## 🏗️ Arquitetura do Workflow

[S3 Bucket] --(ObjectCreated)--> [Lambda Function]
│
▼
Registra logs em CloudWatch


### Explicação:

- **S3 Bucket**: Armazena objetos que acionam a Lambda  
- **Lambda Function**: Processa automaticamente os objetos enviados  
- **IAM Role**: Permite que Lambda acesse o bucket e escreva logs no CloudWatch  

---

## 📄 Arquivo JSON do Template
O template está no arquivo `lambda-s3-automation.json`.  
Ele cria automaticamente S3, Lambda e permissões, além de configurar o **evento de trigger** no S3.

---

## 🧠 Insights e Aprendizados

- Aprendi a criar **triggers S3 → Lambda** automaticamente com CloudFormation  
- Compreendi a importância de **Roles e Policies** para acesso seguro  
- Entendi como **CloudFormation provisiona múltiplos recursos em uma Stack**  
- Aprendi a organizar e documentar o template para reuso futuro  

---

## 📂 Estrutura do Repositório

│── README.md

└── lambda-s3-automation.json

---

## 👩‍💻 Autora
Projeto desenvolvido por **Amanda Justen** — Engenharia de Computação & IA  
LinkedIn: [linkedin.com/in/amanda-justen-80b17182](https://linkedin.com/in/amanda-justen-80b17182)
