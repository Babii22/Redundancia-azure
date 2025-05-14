# ☁️ Projeto Azure Data Engineering - Infraestrutura Completa com Recursos de Dados

## 🧭 Visão Geral

Este projeto tem como objetivo a prática da criação de uma infraestrutura robusta na **nuvem Azure**, focada em **engenharia de dados e machine learning**, abordando desde o conceito de precificação até a implementação de serviços como **Azure Databricks**, **Data Factory**, **Delta Lake**, **AKS**, entre outros.

---

## 💰 Diferença entre Recursos Pagos, Precificação e Métodos de Implementação

No **Microsoft Azure**, os serviços são cobrados com base no **modelo de consumo**, o que significa que você paga pelo que usar. As três principais opções de precificação são:

- 🔄 **Pago conforme o uso (Pay-as-you-go)**: Ideal para cargas variáveis e testes. Você paga por segundo.
- 📉 **Instâncias Reservadas**: Você se compromete com 1 ou 3 anos de uso, recebendo um desconto.
- 💼 **Plano de Economia do Azure**: Preço reduzido com compromisso fixo de gasto por hora.

---

## 🧮 Estimando Custos com a Calculadora do Azure

A [Calculadora de Preços do Azure](https://azure.microsoft.com/pt-br/pricing/calculator/) permite:

- 📦 Simular custos com base na região, número de instâncias e tipo de serviço.
- 📊 Comparar diferentes modelos de precificação.
- 📥 Exportar o orçamento mensal estimado em PDF ou Excel.

---

## 🎓 Onde Estudar e Aprender na Prática

### 📚 Fontes Oficiais:
- Microsoft Learn 

### 🧪 Prática com Conta Gratuita
1. Crie sua conta gratuita
2. Ganhe **R$ 1.000 em créditos por 30 dias**.
3. Acesse serviços gratuitos por 12 meses, como:
   - Azure Data Factory (limite gratuito mensal)
   - Azure Event Hubs (instância básica)
   - Key Vault e Azure Storage (contas de nível gratuito)

---

## 🏗️ Estrutura da Infra Completa (Arquitetura de Engenharia de Dados)

Abaixo, os serviços utilizados na construção da nossa infraestrutura:

| Serviço | Descrição |
|--------|-----------|
| 🔷 **Azure Databricks** | Plataforma para big data e ML com Apache Spark. |
| 📡 **Azure Event Hub** | Ingestão de dados em tempo real (streaming). |
| 💾 **Data Lake Storage** | Armazenamento escalável para dados estruturados e não estruturados. |
| 🧠 **Azure Machine Learning** | Treinamento e gerenciamento de modelos de ML. |
| 🐳 **AKS (Azure Kubernetes Service)** | Orquestração de containers para deploy de modelos e APIs. |
| 🌊 **Delta Lake** | Camada de armazenamento transacional sobre o Data Lake. |
| 🔁 **MLflow** | Controle de experimentos de Machine Learning. |

---

# 🔁 Cópia de Dados On-Premises para Azure Data Lake

## 🧭 Visão Geral

Este projeto documenta o processo de **criação de redundância de arquivos e sincronização de dados** entre um ambiente **on-premises com SQL Server** e a nuvem Azure, utilizando **Azure Data Factory (ADF)** para mover os dados para o **Data Lake Storage Gen2**, com suporte via **Blob Storage** intermediário e pipelines orquestrados.

---

## 🗂️ Estrutura da Solução

Abaixo está o fluxo de ponta a ponta:

1. 🗃️ **SQL Server On-Premises** – Fonte dos dados originais  
2. 🔗 **Self-hosted Integration Runtime (SHIR)** – Gateway de conexão segura com o ambiente local  
3. 🧪 **Azure Data Factory** – Criação de pipelines de movimentação e transformação de dados  
4. 📦 **Blob Storage (opcional)** – Camada temporária de staging (útil para arquivos grandes ou backup)  
5. 🗄️ **Data Lake Storage Gen2** – Destino final para armazenamento redundante e estruturado  
6. 🔁 **Triggers** – Agendamento ou execução contínua das cópias  

---

## 🧱 Etapas de Implementação

### 🔌 1. Criar o **Self-Hosted Integration Runtime**

- Acesse o Azure Data Factory  
- Vá em `Manage > Integration Runtimes > New > Self-hosted > Download`  
- Instale o runtime na máquina com acesso ao SQL Server  
- Copie a **chave de autenticação** gerada e conclua a instalação  

---

### 🛠️ 2. Criar a **Linked Service para SQL Server**

- Tipo: SQL Server  
- Usar o SHIR configurado  
- Fornecer string de conexão, usuário e senha  
- Testar a conectividade  

---

### 📦 3. Criar a **Linked Service para o Data Lake**

- Tipo: **Azure Data Lake Storage Gen2**  
- Método de autenticação:
  - 🔑 Chave de acesso da conta de armazenamento  
  - 🔐 Managed Identity (se disponível e habilitada)  

---

### 🔁 4. Criar o **Pipeline no ADF**

- Atividade principal: **Copy Data**  
- Origem:
  - Criar um Linked Service do SQL Server    
- Destino (Sink):
  - Linked Service do Data Lake   

---

## ✅ Conclusão

Este projeto proporciona uma vivência prática com os principais recursos de engenharia de dados no Azure, desde a estimativa de custos até a implementação de uma infraestrutura real, segura e escalável.

---
