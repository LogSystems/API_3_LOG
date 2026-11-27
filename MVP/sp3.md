# 📌 MVP - LogSystem - Sprint 3

## 🎯 Objetivo do MVP
- Manter a análise em cima do piloto sugerido pelo cliente  
- Trazer as informações de Kms percorridos  


---

## 📝 Descrição da Solução
> Breve explicação do que será desenvolvido e entregue nesta etapa.  
- Piloto limitado as cidades de São José dos Campos, Taubaté e Caçapava
- Métricas utilizadas para otimização: 
| 1 | Jornada de trabalho de 8 horas, sendo 7 horas trabalhadas;|
| 2 | Exclusão de fiscais com baixa participação histórica de verificações;
| 3 | Fixação das equipes, sendo um fiscal para um motorista;|
| 4 | Recálculo das rotas, ligando os pontos de verificação próximos e limitando o tempo de deslocamento e fiscalização à 7 horas por dia;|
| 5 | Redistribuição dos roteiros por equipe, equalizando os serviços de forma equilibrada;|

---

## 👥 Personas / Usuários-Alvo
- **Persona 1:** Gestor do IPEM 


---

| ID  | User Story                                                                 | Prioridade | Estimativa |
|-----|-----------------------------------------------------------------------------|------------|------------|
| US8  | Como gestor do IPEM, quero analisar quais os municípios com maior número de fiscalizações, para entender as cidades onde as equipes mais se concentram.         | Alta       | 5 pontos   |
| US9 | Como gestor do IPEM, quero analisar os tipos de instrumentos mais fiscalizados pelas esquipes, para quantificar as fiscalizações mais realizadas.         | Média      | 5 pontos   |
| US10 | Como gestor do IPEM, quero analisar os tipos de serviço mais prestado por equipe, para dimencionar qual a maior demanda de atividades.         | Média      | 1 pontos   |



---

## 📅 Sprint(s) Relacionadas
| Sprint | Entregas Principais                          | Status   |
|--------|----------------------------------------------|----------|
| 01     | Cartão com os KMs percorridos por equipe                        | Concluído|


---

## 📊 Critérios de Aceitação
- Navegação entre as duas páginas  
- Os filtros devem puxar as informações relacionadas 

---

## 📈 Métricas de Validação
- Número de usuários que testaram o MVP: 3  
- Validação do cliente  

---

## 🚀 Próximos Passos
- Preparar a apresentação para o cliente  


---

## 📝 Relatório (Prévia)
  O desenvolvimento do projeto consiste na análise e otimização dos roteiros
de fiscalização do IPEM-SP, com foco na filial de São José dos Campos e nos
registros referentes ao ano de 2018. Inicialmente, foi realizada a extração,
limpeza e organização dos dados, corrigindo informações inconsistentes e
estruturando os registros de fiscais, motoristas, estabelecimentos e instrumentos
fiscalizados. Em seguida, foi feita a geolocalização dos endereços por meio do
OpenStreetMap, permitindo identificar as coordenadas dos estabelecimentos e
organizar os locais de visitação.

  Com os dados tratados e georreferenciados, foram calculadas as distâncias
percorridas entre os pontos de fiscalização, incluindo os deslocamentos de
ida e volta à base do IPEM-SP. Também foram realizadas verificações para
avaliar a qualidade das coordenadas e a confiabilidade das distâncias estimadas.
Essas informações serviram de base para a construção dos roteiros reais e para
o desenvolvimento de um processo de otimização, com o objetivo de encontrar
trajetos mais eficientes. Por fim, foram estruturadas bases de dados para
alimentar dashboards no Power BI, possibilitando comparar os cenários reais
e otimizados, identificar oportunidades de redução de deslocamentos e avaliar
melhorias na utilização do tempo e dos recursos disponíveis nas atividades
de fiscalização.


---

## 📂 Anexos / Evidências

Relatório:
[Relatório](https://github.com/LogSystems/API_3_LOG/blob/main/Docs/RelatórioSprint3.pdf)

Link vídeo:
[![Assista ao vídeo](<img width="1320" height="852" alt="image" src="https://github.com/user-attachments/assets/f82b2975-95cd-4eec-a267-c2b35ca26ba4" />.)](https://youtu.be/KWjX6C0knbM)






