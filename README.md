
# 🚦 Análise de Acidentes de Trânsito em Belo Horizonte – 2021  
**Clusterização aplicada à segurança viária usando Machine Learning**

Este repositório apresenta os resultados do estudo desenvolvido para o **XLIII ENEGEP (2023)**, com o objetivo de identificar padrões em acidentes de trânsito ocorridos em Belo Horizonte durante o ano de 2021. Foram utilizadas técnicas de **Mineração de Dados** e **Aprendizado de Máquina Não Supervisionado**, visando apoiar tomadas de decisão relacionadas à segurança viária e políticas públicas.

---

## 📄 Objetivo do Projeto

Agrupar acidentes de trânsito com características semelhantes utilizando algoritmos de **clusterização**, permitindo identificar padrões relacionados a:

- Tipo e severidade do acidente  
- Clima e pavimentação da via  
- Datas comemorativas e feriados  
- Tipo e quantidade de veículos envolvidos  
- Perfil dos condutores  
- Índices de fatalidade

---

## 📊 Base de Dados Utilizada

Os dados foram disponibilizados pela Prefeitura de Belo Horizonte no portal de dados abertos. Três conjuntos principais foram processados e consolidados.

| Dataset | Descrição | Registros |
|--------|-----------|----------|
| 1 | Dados gerais do acidente | 11.122 |
| 2 | Características dos indivíduos envolvidos | 23.736 |
| 3 | Informações dos veículos | 20.506 |

Após filtros, tratamento de ausências e normalização:  
➡ **4.562 instâncias finais**  
➡ **31 variáveis pré-processadas**

---

## 🔍 Metodologia

### 🧹 1. Tratamento e Preparação dos Dados
- Junção dos três conjuntos usando Nº do boletim de ocorrência  
- Criação de novas variáveis (horário, contagem de veículos, envolvimento feminino/masculino, embriaguez etc.)  
- Remoção e imputação de dados faltantes  
- Normalização para intervalo `[0,1]`  

### 🤖 2. Modelagem — Clusterização
Algoritmos aplicados:

| Algoritmo | Tipo | Utilização |
|---|---|---|
| K-Means | Não supervisionado | Formação dos clusters principais |
| Hierárquico (Aglomerativo) | Não supervisionado | Análise comparativa de agrupamento |

Número ideal de grupos definido via:

- Método do Cotovelo (Elbow)
- Dendrograma
- Coeficiente Silhouette  
📌 Melhor estrutura: **6 clusters**

---

## 📈 Resultados Relevantes

- Regiões com maior volume de acidentes estão concentradas na área **Centro-Sul de BH**
- Acidentes apresentaram variação significativa em relação ao **clima**
- **Atropelamentos em dias chuvosos mostraram maior taxa de fatalidade**
- Feriados apresentaram incidência ligeiramente maior de ocorrências
- **Homens estiveram presentes em ~95% dos casos analisados**
- Clusters distintos foram formados com base em tipo de acidente, pavimento e severidade

---

## 🧠 Ferramentas Utilizadas

| Tecnologia | Finalidade |
|---|---|
| Python + Jupyter Notebook | Análise exploratória e clustering |
| Pandas / NumPy | Tratamento e organização dos dados |
| sklearn (Scikit-Learn) | Execução dos algoritmos de clusterização |
| Matplotlib / Seaborn | Visualização gráfica |
| Excel | Pré-tratamento inicial dos datasets |

---

## 📎 Documento do Artigo

📄 **Arquivo incluído no repositório:**  
`Acidentes BH Corpo-Artigo-ENEGEP-2023-FINAL.pdf`

---

## 🚀 Próximos Passos (Possíveis Extensões)

- Análise preditiva com modelos supervisionados  
- Dashboard interativo com Streamlit / Power BI / Dash  
- Inclusão de dados dos próximos anos para estudo evolutivo  
- Georreferenciamento com mapas interativos

---

## 📌 Autor(es)

Este repositório documenta o estudo acadêmico voltado para análise de acidentes urbanos utilizando ciência de dados aplicada ao transporte.

📬 Contribuições, issues e melhorias são bem-vindas!
