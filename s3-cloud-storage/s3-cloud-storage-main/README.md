#  Atividade Prática de Site Estático com Amazon S3 

Este repositório contém os arquivos e instruções utilizados na **atividade prática do módulo Amazon S3**, realizada pelos alunos do curso **AWS re/Start**.

##  Descrição da Atividade

Esta atividade prática tem como objetivo reforçar o conteúdo do módulo **Amazon S3**, colocando em prática os conceitos de criação de buckets, permissões, políticas públicas e hospedagem de sites estáticos na nuvem.  
Os alunos devem criar, configurar e publicar seu próprio site em HTML/CSS usando um bucket no S3.

---

## 🚀 Objetivo

Aprender a configurar e hospedar um site estático  no **Amazon S3**, tornando-o acessível publicamente.

---

## 📘 O que você vai aprender

- O que é o Amazon S3
- Diferença entre sites estáticos e dinâmicos
- Como criar um bucket S3 e configurar a hospedagem estática
- Como lidar com erro 403 (Access Denied)
- Como aplicar uma política pública de leitura

---

## ☁️ O que é o Amazon S3?

O **Amazon S3 (Simple Storage Service)** é um serviço da AWS que permite armazenar arquivos na nuvem de forma segura, escalável e acessível. Ideal para guardar imagens, vídeos, documentos e também hospedar sites estáticos.

---

## 🧱 O que é um site estático?

Um **site estático** é composto apenas por arquivos HTML, CSS e JavaScript. Ele não depende de servidores ou bancos de dados para gerar conteúdo dinâmico, tornando-se leve, rápido e de baixo custo.

**Exemplos**:
- Portfólios pessoais
- Currículos online
- Landing pages
- Sites institucionais simples

---

## 🧰 Tecnologias Utilizadas

- **Amazon S3 (AWS)**
- **HTML5**
- **CSS3**
- **AWS Console**

---

## 📁 Conteúdo do Repositório

- `index.html` – Página principal do site
- `img/` – Pasta com imagens utilizadas no projeto

📥 [Clique aqui para baixar os arquivos do site (index.html + img)](https://drive.google.com/drive/folders/1LT7v9PolbKJLIoSGOQUt3JqftrwkerxZ?usp=sharing)

---

## 🧪 Etapas da Atividade

### 1️⃣. Criar um Bucket no Amazon S3

- Acesse o [Console da AWS](https://aws.amazon.com/console/)
- Vá para **S3 > Criar bucket**
- Escolha um nome único, ex: `my-cloud-website`
- Desmarque a opção **"Bloquear acesso público"**
- Finalize com configurações padrão


---

### 2️⃣. Fazer Upload dos Arquivos

- Faça upload de:
  - `index.html`
  - Pasta `img/` com imagens


---

### 3️⃣. Ativar Hospedagem Estática

- Vá até **Propriedades** do bucket
- Ative **Hospedagem de site estático**
- Configure:
  - Documento de índice: `index.html`
  - Documento de erro: `error.html` (opcional)
- Copie o **Endpoint**


---
### Tentar acessar o site
Você verá um erro:  

❗
 POR QUE ISSO ACONTECE? 
Sem uma política de permissão pública no bucket, ninguém pode acessar os 
arquivos, nem mesmo o site estático.


### 4️⃣. Corrigir Erro 403 com Política Pública

Caso o site retorne erro de acesso (403 Access Denied):

- Vá até **Permissions > Bucket Policy**
- Insira a seguinte política (troque o nome do bucket):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::my-bucketname/*"
    }
  ]
}

```

Substitua my-bucketname pelo nome real do seu bucket.

- Salve a política

### 5️⃣. Acessar o Site Publicado 🎉
Volte para Propriedades > Hospedagem de site estático

Acesse o link do Endpoint

### 👍 Parabéns!
Você concluiu com sucesso Atividade Publicação de Site Estático com Amazon S3 

###  Por que isso é importante?

> Compreender como hospedar arquivos na nuvem de forma simples e rápida  
> 
> Aprender sobre controle de acesso e permissões em buckets S3  
> 
> Desenvolver habilidades práticas em cloud computing com foco em **armazenamento e entrega de conteúdo**  
> 
> Avançar na trilha rumo à **certificação AWS Cloud Practitioner**  

---

## 🛠 Tecnologias Utilizadas

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" alt="AWS" width="80" height="60"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML" width="60" height="60"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" alt="Bash" width="60" height="60"/>
</p>

---

