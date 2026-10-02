---
title: "[]{#_Toc118654374 .anchor}Relatório -- logsystem -- 1° sprint"
---

Thiago Moreira - linkedin.com/in/thiago-fernandes-moreira-6a1976191

Luiz Felipe Pacheco - linkedin.com/in/luiz-felipe-pacheco-5a285522b

Luiz Henrique Soares - linkedin.com/in/luiz-henrique-soares-45747337a

Pedro Henrique Affonso - linkedin.com/in/pedro-henrique-rocha-affonso-a30758361

Caio Cesár - linkedin.com/in/caio-césar-96a521379

Professor M2 ou Orientador: Carlos Eduardo Bastos

Professor P2: Marcus Nascimento

Resumo do projeto:

O projeto LogSystem consiste no desenvolvimento, por uma equipe, de um painel visual em Power BI voltado a resolver dificuldades enfrentadas pelo Instituto de Pesos e Medidas do Estado de São Paulo (IPEM-SP) no acompanhamento de suas fiscalizações. O objetivo é oferecer ao instituto uma ferramenta de visualização que facilite a análise das atividades de fiscalização e apoie o trabalho cotidiano. O painel apresenta as fiscalizações realizadas por cidade, as fiscalizações realizadas por equipe e os resultados dessas fiscalizações. O desenvolvimento é organizado em sprints e utiliza a linguagem Python, executada na plataforma Databricks, para tratar os dados antes de sua exibição no Power BI. O tratamento separa as duplas de fiscais em equipes e divide os endereços em colunas próprias, preparando-os para os visores de mapas. Na primeira sprint, a equipe obteve um visor que atende às necessidades definidas para essa etapa. Os resultados parciais indicam que a combinação entre tratamento de dados em Python e visualização em Power BI responde às demandas iniciais do IPEM-SP. As próximas etapas consistem em aprimorar o painel no Power BI para entregar as funcionalidades das sprints restantes. Conclui-se que o projeto avança com a primeira entrega concluída e as demais em desenvolvimento.

Palavras-Chave: LogSystem; IPEM-SP; Power BI; Python; fiscalizações; sprints.

Abstract:

The LogSystem project consists of a team developing a visual dashboard in Power BI to address difficulties faced by the Institute of Weights and Measures of the State of São Paulo (IPEM-SP) in monitoring its inspections. The objective is to provide the institute with a visualization tool that facilitates the analysis of inspection activities and supports daily work. The dashboard presents the inspections carried out by city, the inspections carried out by team, and the results of these inspections. The development is organized into sprints and uses the Python language, run on the Databricks platform, to process the data before it is displayed in Power BI. The processing groups the inspector pairs into teams and splits addresses into separate columns, preparing them for the map visuals. In the first sprint, the team delivered a viewer that meets the needs defined for that stage. Partial results indicate that combining data processing in Python with visualization in Power BI responds to the initial demands of IPEM-SP. The next steps consist of improving the dashboard in Power BI to deliver the features of the remaining sprints. The project is therefore progressing, with the first delivery completed and the others under development.

Keywords: LogSystem; IPEM-SP; Power BI; Python; inspections; sprints.

# Contextualização do projeto

O Instituto de Pesos e Medidas do Estado de São Paulo (IPEM-SP) é uma autarquia do Governo do Estado e órgão delegado do Inmetro, responsável por fiscalizar instrumentos de medição, como balanças, bombas de combustível e taxímetros, verificando se medem corretamente e se estão dentro das tolerâncias permitidas (IPEM-SP, 2026). O instituto também fiscaliza produtos pré-medidos, como alimentos vendidos por peso ou volume, conferindo se a quantidade indicada na embalagem corresponde ao conteúdo, além de acompanhar a medição na comercialização de combustíveis e o cumprimento de normas de metrologia e qualidade (IPEM-SP, 2026). Dessa forma, a atividade de fiscalização protege o consumidor e garante a lisura das relações comerciais.

Nesse contexto, a gestão dessas fiscalizações envolve desafios logísticos, pois exige organizar as equipes, planejar os deslocamentos entre cidades e garantir a cobertura do território. Ressalta-se, porém, que os dados das fiscalizações se encontravam espalhados e eram reunidos em relatórios manuais, o que dificultava a visão consolidada por cidade e por equipe.

Esse projeto aborda, por meio do tratamento de dados em Python e da criação de um painel visual em Power BI, como a organização e a visualização das informações podem apoiar o planejamento das equipes e das rotas de fiscalização do IPEM-SP.

# Objetivos do projeto

Os objetivos estabelecidos para esse projeto consistem em:

i)  Desenvolver um painel visual em Power BI que apresente as fiscalizações realizadas pelo IPEM-SP por cidade, por equipe e seus resultados, apoiando o acompanhamento e o planejamento das atividades de fiscalização;

ii) Desenvolver o tratamento dos dados das fiscalizações utilizando a linguagem Python, organizando informações que antes se encontravam espalhadas e eram consolidadas em relatórios manuais.

# Fundamentação dos métodos analíticos e das tecnologias utilizadas

## Tecnologias da Informação

O projeto utiliza três tecnologias da informação: a plataforma Databricks, a linguagem Python e o Power BI. A plataforma Databricks foi escolhida como ambiente para escrever os códigos Python devido à abrangência de suas ferramentas, e nela a base de dados foi importada para o Catalog, que organiza os arquivos de trabalho. Os códigos utilizam a biblioteca PySpark, incluindo seus módulos de funções e de janelas (Window), para tratar os dados antes de sua exibição.

O Power BI é empregado na construção do painel visual. O painel possui dois filtros, um por equipe e outro pela data da verificação, que permitem selecionar as equipes operantes e as datas em que as verificações foram realizadas. Em seguida, apresenta três gráficos de barras baseados na contagem de serviços: os serviços realizados por cidade, as fiscalizações realizadas por equipe e o resultado das fiscalizações (aprovado, reprovado, interditado, excluído e sem verificação). O painel inclui ainda um mapa que mostra as cidades que mais receberam fiscalizações, com o tamanho de cada círculo definido pela quantidade de endereços geocodificados. Esses visores dependem do tratamento feito em Python, que transforma os dados para que o Power BI os leia corretamente, inclusive o mapa, que exige endereços separados em colunas.

Na primeira sprint, a combinação dessas tecnologias resultou em um visor que atende às necessidades definidas para essa etapa. Os primeiros resultados mostram que a maior parte das fiscalizações teve o resultado aprovado e que São José dos Campos concentra o maior número de serviços realizados entre as cidades. A principal dificuldade encontrada na aplicação das tecnologias foi o tratamento dos dados, etapa que exigiu transformar a base fornecida pelo IPEM-SP para que o Power BI a lesse corretamente, como na separação das duplas fiscalizadoras em equipes e na decomposição da coluna de endereços.

# Coleta e descrição dos dados utilizados

A base de dados utilizada reúne os registros das fiscalizações do IPEM-SP e foi importada para o Catalog da plataforma Databricks, onde ficou disponível para o tratamento em notebooks Python. Entre as informações da base estão o fiscal e o motorista responsáveis por cada fiscalização, a data da verificação, o resultado e o endereço completo do local fiscalizado. As datas de verificação registradas começam em janeiro de 2018.

O objetivo do tratamento foi retirar as informações que não seriam úteis e transformar alguns dados para que o Power BI os lesse corretamente. Na primeira sprint, a base foi importada para o notebook e definida como o DataFrame de trabalho, e em seguida foram removidas as colunas desnecessárias: INDICEDOC, RLD_ID, COD_PROPR e NR_CGC_INDICE. Depois, as duplas fiscalizadoras foram separadas em equipes. Como cada dupla fixa de fiscal e motorista representa uma equipe, o código gerou as combinações únicas dessas duas colunas, numerou-as sequencialmente (Equipe 01, Equipe 02 e assim por diante) e associou cada registro à sua equipe, o que permite quantificar as equipes que operaram no período analisado.

Por fim, a coluna de endereço completo foi decomposta, por meio de expressões regulares, em logradouro, número, cidade e CEP, e a partir dessas colunas foi montado um endereço padronizado para geocodificação, necessário para os visores de mapas. Como conclusão desses tratamentos, foram identificadas as equipes em operação no período analisado, e cada registro passou a ter cidade e equipe em colunas próprias, o que viabiliza os visores por cidade e por equipe.

# Resultados esperados

Espera-se concluir, ao longo das próximas sprints, um painel em Power BI que atenda integralmente às necessidades do IPEM-SP, oferecendo uma visão consolidada das fiscalizações por cidade, por equipe e de seus resultados. Com isso, espera-se reduzir a dependência de relatórios manuais e facilitar a consulta a dados que antes se encontravam espalhados.

Como contribuição técnica, o projeto propõe um processo de tratamento de dados em Python integrado a um painel em Power BI, que apoia o planejamento das equipes, dos deslocamentos entre cidades e da cobertura territorial das fiscalizações. Como contribuição acadêmica, o projeto demonstra a aplicação de ferramentas de análise e visualização de dados à gestão logística de uma atividade de fiscalização pública.
