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

## ♻️ Redundância e Recuperação de Arquivos

Para garantir **resiliência e continuidade**, implemente:

- ✅ **Geo-Redundância (GRS)** no Azure Storage: cópias automáticas dos dados em outra região.
- 🧬 **Versionamento de arquivos** com Delta Lake.
- 📁 **Snapshots** periódicos do Data Lake.
- 🔁 Estratégias de **backup agendado** com Recovery Services Vault.

---

## ✅ Conclusão

Este projeto proporciona uma vivência prática com os principais recursos de engenharia de dados no Azure, desde a estimativa de custos até a implementação de uma infraestrutura real, segura e escalável.

---
