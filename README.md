# Miniprojeto_Gilberto-Barreto_QA-VDBI-2026-1-T3
Mini-Projeto Avaliativo do curso: Visualização de Dados e Business Intelligence [T3] - Semama 1 Módulo 7 

#Análise Exploratória de Dados de Varejo

## Aluno

**Gilberto Barreto**

## Curso

Visualização de Dados e Business Intelligence

## Projeto

Análise Exploratória de Dados aplicada a uma base de Varejo utilizando Python e pandas.

---

## 📁 Arquivos entregues

- `[MS_07]_Mini_Projeto_Avaliativo.ipynb` – notebook contendo o desenvolvimento completo do projeto.
- `df_limpo.csv` – base resultante do tratamento dos dados.
- `README_Gilberto-Barreto_QA-VDBI-2026-1-T3.md` – documentação completa do projeto.

---

## 🎯 Objetivo

Realizar uma Análise Exploratória da base Varejo, contemplando:

- carregamento e exploração inicial dos dados;
- identificação de valores nulos e inconsistências;
- análise de duplicatas;
- tratamento dos dados;
- conversão de tipos;
- estatísticas descritivas;
- agrupamentos;
- análise temporal;
- identificação dos principais insights;
- reflexão sobre ETL e qualidade dos dados.

---

## 🔎 Principais procedimentos realizados

A base original possui **830.000 registros e 14 colunas**.

Durante a exploração foram identificados valores ausentes, registros com `#N/D`, duplicatas e necessidade de conversão da coluna `DATA` para datetime.

Foram encontrados:

- **4 colunas** com valores nulos
- **3.650 registros associados ao `PR_ID` 107** com informações de produto classificadas como `#N/D`;
- **96.553 registros duplicados**.

As colunas com todos os registros com valores nulos foram excluídas.
Os registros contendo informações ausentes (como `#N/D`) foram tratados na criação da base `df_limpo`, que passou a possuir **826.350 registros**.
Foi mantida também a base `df` com todos os registros **830.000 registros** para análises que dependem de dados que são válidos.
As duplicatas foram analisadas e não removidas indiscriminadamente, pois não foi possível determinar que todos os registros repetidos representavam erros.

---

## 📊 Principais resultados

### Número de filhos dos clientes

| Estatística | Resultado |
|---|---:|
| Média | 1,14654 |
| Mediana | 0 |
| Moda | 0 |
| Desvio padrão | 1,41696 |
| Mínimo | 0 |
| Máximo | 4 |
| Contagem | 830.000 |

### Agrupamento por gênero

| Gênero | Quantidade |
|---|---:|
| Feminino (F) | 432.576 |
| Masculino (M) | 397.424 |

Também foi realizado agrupamento por período para analisar a variação da quantidade de compras ao longo do tempo.

---

## 💡 Insights

- A base possui **830.000 registros** e apresenta problemas de qualidade que precisam ser considerados antes de análises posteriores.
- Foram encontrados **3.650 registros com informações de produto classificadas como `#N/D`**.
- A quantidade de filhos apresentou **média de aproximadamente 1,15**, com mediana e moda iguais a zero.
- O gênero feminino apresentou maior quantidade de registros de compras, com **432.576 registros** contra **397.424 do gênero masculino**.
- A quantidade de registros de compras varia ao longo do período analisado, precisando de mais atenção quanto às reduções significativas nos períodos 01/2019, 11/2019, 07/2020, 08/2022 e 09/2022 em que houve o menor patamar registrado de 1.442 unidades. Quanto às categorias de produtos, a categoria de Alimentos lidera amplamente as vendas com 434.767 unidades, enquanto a de Acessórios registra o menor volume, com apenas 14.557 unidades.
- Permaneceram **96.553 registros duplicados**, pois não foi possível determinar que todas as duplicidades representavam erros.

---

## 🔄 Reflexão sobre ETL

O projeto pode ser relacionado às três etapas do processo ETL:

**Extract:** carregamento da base de varejo utilizando pandas e exploração inicial dos dados.

**Transform:** identificação e tratamento de problemas de qualidade, conversão de tipos, tratamento de valores ausentes e preparação dos dados para análise.

**Load:** geração da base `df_limpo` e a permanência da base `df` com as transformações essenciais, mas mantendo todos os registros , que podem ser utilizadas posteriormente em análises e ferramentas de Business Intelligence, a depender da análise feita.

---

## 🧹 Qualidade dos dados

A análise demonstrou que a qualidade dos dados é fundamental para a obtenção de resultados confiáveis.

Valores ausentes, informações inconsistentes, tipos inadequados e duplicidades podem afetar as análises.

Neste projeto, os valores ausentes (`#N/D) relacionados aos produtos/categoria, para a base df_limpo, foram tratados por meio da remoção dos registros, pois não havia informações suficientes para realizar uma imputação confiável.

As duplicidades foram mantidas quando não havia evidência suficiente de que representavam erros, evitando a remoção indevida de registros potencialmente válidos.

---

## ▶️ Como executar

O projeto foi desenvolvido no **Google Colab**.

Para executar:

1. Abrir o notebook `[MS_07]_Mini_Projeto_Avaliativo.ipynb`;
2. Abrir o arquivo no Google Colab;
3. O `Base Varejo.csv` já está disponível no código por meio da Importação do arquivo direto do Kaggle;
4. Executar as células do notebook em ordem.

---

## 🔗 Links

**GitHub:**  
https://github.com/gilgraca-datascience/Miniprojeto_Gilberto-Barreto_QA-VDBI-2026-1-T3

**Google Colab:**
https://colab.research.google.com/drive/1WOtzyeyhjgBzqikt1Pdg38mBJPKo83uC?usp=sharing
---

## 👨💻 Autor

**Gilberto Barreto**

Mini-Projeto Avaliativo – Módulo 1 – Semana 07
