Análise de Acidentes de Trânsito em Belo Horizonte (2021)
Clusterização aplicada à segurança viária utilizando Machine Learning

Este repositório contém a análise apresentada no artigo desenvolvido para o XLIII Encontro Nacional de Engenharia de Produção (ENEGEP – 2023), cujo objetivo foi identificar padrões em acidentes de trânsito ocorridos na cidade de Belo Horizonte (MG) durante o ano de 2021.

Por meio de técnicas de Mineração de Dados e Aprendizado de Máquina não supervisionado, foi possível agrupar acidentes com características semelhantes, favorecendo interpretações relevantes para o setor público, segurança urbana, e gestão de tráfego.

Objetivo do estudo

Agrupar acidentes de trânsito em Belo Horizonte utilizando K-Means e Clusterização Hierárquica, para identificar padrões associados a:

Tipo e severidade do acidente

Condições climáticas

Pavimentação e horário

Quantidade e tipo de veículos envolvidos

Presença de feriados e finais de semana

Frequência de fatalidades

O estudo visa apoiar políticas públicas com base em evidências, fornecendo insights úteis para estratégias de prevenção e redução de riscos.

Base de Dados

Foram utilizados três conjuntos de dados públicos, disponibilizados pela Prefeitura de Belo Horizonte, totalizando mais de 11 mil registros iniciais, posteriormente tratados e unificados.

Dataset	Conteúdo	Instâncias
1	Características do acidente	11.122
2	Características dos indivíduos	23.736
3	Características dos veículos	20.506

Após limpeza, criação de novas variáveis e normalização, o conjunto final contou com:

✔ 4.562 registros
✔ 31 variáveis tratadas e padronizadas

🔍 Metodologia

Pré-processamento e fusão das bases

Tratamento de dados ausentes

Geração de novas variáveis

Normalização no intervalo [0,1]

Aplicação dos algoritmos

K-Means

Hierarchical Clustering (aglomerativo)

Definição do número de grupos

Método do Cotovelo (Elbow)

Dendrograma

Métrica da Silhueta ✓ melhor desempenho com 6 clusters

Principais Resultados

🔹 Os dois algoritmos apresentaram agrupamentos semelhantes
🔹 Acidentes foram influenciados por clima, pavimentação e feriados
🔹 Atropelamentos em dias de chuva mostraram maior índice de fatalidade
🔹 A região Centro-Sul concentrou mais ocorrências, refletindo maior tráfego urbano
🔹 Homens estiveram envolvidos em quase 95% dos acidentes

Tecnologias utilizadas
Ferramenta	Uso
Python + Jupyter	Análise e Clusterização
Pandas / NumPy	Pré-processamento
Scikit-Learn	Modelagem e agrupamento
Matplotlib / Seaborn	Visualização gráfica
Excel	Limpezas preliminares

README elaborado com base do meu artigo publicado: https://doi.org/10.14488/ENEGEP2023_TN_ST_401_1975_46517
