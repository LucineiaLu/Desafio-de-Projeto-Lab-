https://colab.research.google.com/drive/1cpD0MdWS7ZdLYBqTJ5Q0wLmeL3qbaYaz?usp=sharing


# Desafio-de-Projeto-Lab-
# 🚀 Explorando IA Generativa em um Pipeline de ETL com Python

> Projeto destaque inspirado no desafio prático da **Digital Innovation One (DIO)**, com foco em **ETL, Python e IA Generativa**, desenvolvido para compor portfólio profissional.


## 📌 Descrição do Desafio

Neste projeto, o objetivo é construir um **pipeline ETL completo (Extract, Transform, Load)** aplicando conceitos de **IA Generativa** na etapa de transformação dos dados.

O desafio original utiliza APIs externas (como OpenAI/GPT). Nesta versão, o projeto foi **reimaginado e adaptado** para funcionar **sem dependência de APIs externas**, mantendo o foco didático, acessível e alinhado às boas práticas exigidas pelo mercado.



## 🎯 Objetivo

Demonstrar, de forma prática, a aplicação de:

* Processos de **ETL**
* **Python** aplicado à Engenharia de Dados
* Uso criativo de **IA Generativa (simulada)**
* Organização de projeto no padrão exigido para **desafios da DIO**

O pipeline simula a análise de **feedbacks de clientes**, gerando **classificação de sentimento** e **insights automáticos** para apoio à tomada de decisão.



## 🧠 Tecnologias Utilizadas

* **Python 3.x**
* **Pandas** – manipulação e transformação de dados
* **SQLite** – persistência local dos dados



## 🏗️ Estrutura do Projeto

```text
📁 pipeline-etl-ia-generativa
│
├── etl_ia_generativa.py        # Script principal do pipeline ETL
├── feedbacks_clientes.csv     # Dados de entrada (gerado automaticamente)
├── feedbacks_tratados.csv     # Dados finais transformados
├── feedbacks.db               # Banco de dados SQLite
└── README.md                  # Documentação do projeto
```



## 🔄 Etapas do Pipeline ETL

### 🔹 Extract (Extração)

* Leitura de dados a partir de um arquivo CSV;
* Caso o arquivo não exista, o pipeline cria automaticamente um dataset de exemplo.



### 🔹 Transform (Transformação com IA Generativa Simulada)

Nesta etapa ocorre o principal diferencial do projeto:

* Análise de sentimento dos comentários (Positivo, Negativo ou Neutro);
* Geração automática de **insights textuais**, simulando o comportamento de uma IA Generativa;
* Aplicação de regras de negócio e padronização dos dados.

> ⚠️ Não há consumo de APIs externas. Toda a lógica é implementada localmente em Python.



### 🔹 Load (Carga)

Os dados transformados são carregados em:

* 📄 Arquivo CSV
* 🗄️ Banco de dados SQLite

Esses formatos permitem integração futura com ferramentas de BI e dashboards.



## ▶️ Como Executar o Projeto

### 1️⃣ Clonar o repositório

```bash
git clone https://github.com/seu-usuario/pipeline-etl-ia-generativa.git
cd pipeline-etl-ia-generativa
```

### 2️⃣ Instalar dependências

```bash
pip install pandas
```

### 3️⃣ Executar o pipeline

```bash
python etl_ia_generativa.py
```

---

## 📊 Exemplo de Resultado

| id_cliente | comentario                           | sentimento | insight                                         |
| ---------: | ------------------------------------ | ---------- | ----------------------------------------------- |
|          1 | Entrega rápida e produto excelente   | Positivo   | Cliente satisfeito. Manter padrão de qualidade. |
|          2 | Atendimento ruim e atraso na entrega | Negativo   | Revisar processos de atendimento e logística.   |



## 🌟 Diferenciais (Padrão Projeto Destaque DIO)

✔ Pipeline ETL completo e funcional
✔ Uso criativo de IA Generativa (simulada)
✔ Código limpo, organizado e comentado
✔ Não depende de serviços pagos
✔ Fácil adaptação para outros domínios (saúde, educação, logística)
✔ Ideal para portfólio e entrevistas técnicas



## 🚀 Possíveis Evoluções

* Integração com APIs reais de IA Generativa
* Uso de NLP com spaCy ou NLTK
* Conexão com Data Warehouses
* Criação de dashboards interativos



## 👩‍💻 Autora

**Lucineia**
Projeto desenvolvido como desafio prático e projeto de portfólio no contexto da **Digital Innovation One (DIO)**.



📢 *Projeto desenvolvido para fins educacionais e demonstração de competências técnicas.*

