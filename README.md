# EpiData Intelligence
# Epidemiological and Immunization Data Analytics

O EpiData Intelligence é um projeto acadêmico desenvolvido como
parte de um Trabalho de Conclusão de Curso (TCC), com foco na
integração, organização e análise de dados epidemiológicos e de
imunização para apoiar a vigilância em saúde pública no estado de
Pernambuco, Brasil.

O projeto aplica conceitos de Data Mart, Business Intelligence
(BI) e Processamento Analítico Online (OLAP) para explorar padrões
de ocorrência de agravos, vacinação e indicadores de saúde pública.

Visão geral

A vigilância epidemiológica depende de dados provenientes de diferentes
sistemas, que podem apresentar estruturas, níveis de detalhamento e
períodos de referência distintos. O EpiData Intelligence busca organizar
esses dados em um ambiente analítico dimensional, facilitando consultas
e análises temporais e geográficas.
O estudo concentra-se em:
- Agravos: sarampo e coqueluche.
- Abrangência geográfica: municípios do estado de Pernambuco,
  Brasil.
- Período de estudo: 2010--2025, respeitando a disponibilidade e a comparabilidade
  dos dados de cada fonte.
- Abordagem: integração de dados, modelagem dimensional, consultas
  analíticas, cálculo de indicadores e visualização interativa.

Objetivos
- Integrar dados epidemiológicos, de vacinação, de cobertura vacinal e
  populacionais provenientes de fontes públicas de saúde.
- Organizar os dados analíticos em um Data Mart dimensional.
- Apoiar o cálculo e a análise de indicadores epidemiológicos e de
  imunização.
- Permitir análises por município, ano, agravo e imunobiológico,
  conforme o nível de detalhamento disponível nas fontes.
- Oferecer uma base para painéis interativos e para a tomada de
  decisão fundamentada em dados na área da saúde pública.

Fontes de dados

- SINAN --- notificações epidemiológicas e registros relacionados
  aos agravos.
- RNDS / OpenDataSUS --- registros individuais de vacinação
  disponíveis nos conjuntos de dados publicados.
- SI-PNI / TABNET / DATASUS --- informações agregadas oficiais
  sobre vacinação, cobertura vacinal e populacional, utilizadas em análises
  históricas e comparações.
- Dados geográficos --- informações sobre os municípios do Estado de Pernambuco.

A disponibilidade, as definições, a granularidade e a cobertura temporal
variam entre as fontes. Por isso, os registros individuais de vacinação
e as estatísticas históricas agregadas são tratados como tipos distintos
de dados, sem pressupor que sejam diretamente intercambiáveis.

Modelagem dimensional do Data Mart

O modelo dimensional está organizado em torno de quatro tabelas fato:

 - Fato Populacional: Armazenar medidas populacionais utilizadas como
  denominadores de indicadores selecionados.
  
 - Fato Cobertura Vacinal: Armazenar medidas agregadas de cobertura vacinal
  provenientes de fontes históricas oficiais.
  
 - Fato Epidemiologia: Armazenar medidas derivadas dos registros
  epidemiológicos, como casos confirmados e óbitos.
  
 - Fato Vacinação: Armazenar eventos individuais de vacinação e medidas
  quantitativas disponíveis nas fontes.

As dimensões e os relacionamentos analíticos permitem consultar os dados
por tempo, município, agravo e imunobiológico, respeitando a
granularidade de cada conjunto de dados.

Indicadores implementados

- Coeficiente de incidência
- Taxa de letalidade
- Cobertura vacinal
- Homogeneidade da cobertura entre municípios

Os indicadores são calculados somente quando os numeradores,
denominadores e definições necessários estão disponíveis e apresentam
consistência suficiente.

Tecnologias utilizadas

- PostgreSQL --- banco de dados relacional e armazenamento do Data
  Mart.
- Pentaho Data Integration (PDI / Spoon) --- extração,
  transformação e carga de dados (ETL).
- Power BI --- construção de painéis interativos e análises
  visuais.

Banco de dados do projeto

O banco de dados do projeto pode ser acessado a partir do link:
https://drive.google.com/drive/folders/1eYp1o5CsMrgZXWeu35DuW5fGXAsq24Nv?usp=drive_link

Reprodutibilidade e uso responsável

Para reproduzir o fluxo de trabalho:
1. Obtenha os conjuntos de dados em suas fontes oficiais.
2. Consulte a documentação, as definições e os períodos de
   referência de cada fonte.
3. Configure o PostgreSQL e ajuste as conexões utilizadas nos fluxos
   ETL.
4. Execute as transformações na ordem prevista e valide as tabelas
   resultantes.

O projeto tem finalidade acadêmica e de apoio à exploração analítica.
Seus resultados não substituem publicações epidemiológicas oficiais nem
a avaliação de profissionais de saúde pública.

Contexto acadêmico

O EpiData Intelligence integra um Trabalho de Conclusão de Curso (TCC)
sobre a aplicação de técnicas de Data Mart e Business Intelligence à
vigilância epidemiológica e à análise de imunização em Pernambuco,
Brasil.

Licença

Este projeto está licenciado sob a Licença MIT - consulte o arquivo [LICENSE](LICENSE) para obter mais detalhes.
