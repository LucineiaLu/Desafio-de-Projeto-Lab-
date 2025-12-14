# Desafio-de-Projeto-Lab-
🔹 Projeto: IA Generativa Aplicada a um Pipeline de ETL com Python
🎯 Objetivo do Projeto

Desenvolver um pipeline de ETL em Python, aplicando conceitos de IA Generativa na etapa de Transformação, simulando inteligência de negócio e enriquecimento de dados, sem depender diretamente de APIs externas como OpenAI.

🔹 Domínio de Aplicação (Novo Contexto)

Análise de Feedbacks de Clientes de uma Loja Online

O pipeline irá:

Extrair dados de clientes e comentários

Transformar os dados usando IA Generativa simulada (classificação de sentimentos e geração de insights)

Carregar os dados tratados em um arquivo final ou banco de dados

🔹 Arquitetura do Pipeline ETL
[CSV / Excel / JSON]
        ↓
     EXTRACT
        ↓
  TRANSFORM (IA Generativa)
        ↓
      LOAD
 [CSV / SQLite / DataFrame]

🔹 1. Extract – Extração dos Dados

📌 Fonte de dados simulada: feedbacks_clientes.csv

Exemplo de dados:

id_cliente	comentario
1	Entrega rápida e produto excelente
2	Atendimento ruim e atraso na entrega
import pandas as pd

df = pd.read_csv("feedbacks_clientes.csv")
df.head()

🔹 2. Transform – IA Generativa (Sem API Externa)

Aqui está o diferencial do projeto 💡
Em vez de usar GPT via API, você pode:

✔️ Simular IA Generativa com regras inteligentes
✔️ Usar NLP básico (TextBlob, spaCy ou regras manuais)
✔️ Criar funções que “imitam” comportamento generativo
🔹 Exemplo: Classificação de Sentimento Simulada
def analisar_sentimento(texto):
    texto = texto.lower()
    
    if "excelente" in texto or "ótimo" in texto or "rápida" in texto:
        return "Positivo"
    elif "ruim" in texto or "atraso" in texto:
        return "Negativo"
    else:
        return "Neutro"

df["sentimento"] = df["comentario"].apply(analisar_sentimento)

🔹 Exemplo: Geração de Insight (IA Generativa Simulada)
def gerar_insight(sentimento):
    if sentimento == "Positivo":
        return "Cliente satisfeito. Manter padrão de qualidade."
    elif sentimento == "Negativo":
        return "Cliente insatisfeito. Revisar processos de atendimento."
    else:
        return "Avaliação neutra. Monitorar experiência do cliente."

df["insight"] = df["sentimento"].apply(gerar_insight)

🔹 3. Load – Carregamento dos Dados
✔️ Opção 1: CSV Final
df.to_csv("feedbacks_tratados.csv", index=False)

✔️ Opção 2: Banco de Dados SQLite
import sqlite3

conn = sqlite3.connect("feedbacks.db")
df.to_sql("analise_feedbacks", conn, if_exists="replace", index=False)
conn.close()

🔹 Estrutura do Repositório GitHub
📁 ia-generativa-etl-python
│
├── data/
│   ├── feedbacks_clientes.csv
│   └── feedbacks_tratados.csv
│
├── etl_pipeline.py
├── requirements.txt
└── README.md

🔹 README.md (Resumo Sugerido)
## Pipeline ETL com IA Generativa em Python

Projeto desenvolvido para explorar conceitos de ETL e IA Generativa
aplicados à análise de feedbacks de clientes, sem dependência de APIs externas.

### Tecnologias:
- Python
- Pandas
- SQLite

### Etapas:
- Extract: Leitura de dados CSV
- Transform: Classificação de sentimentos e geração de insights
- Load: Armazenamento em CSV e SQLite
