Trabalho Final de Inteligência Artificial
====================================================

Disciplina do Mestrado em Computação Aplicada - IFES (PPCOMP)

## Detecção de anomalias em um sinal temporal de processo industrial utilizando técnica de agrupamento (*Clustering*) 

A proposta deste trabalho é de avaliar uma série temporal multivariada proveniente de sinais gerados por sensores de um processo industrial de produção de aço, buscando identificar situações anômalas no comportamento destes sinais.

### Abordagem
A abordagem a ser utilizada para identificação será o uso de uma técnica de aprendizado de máquina não supervisionada, neste caso agrupamento (*clustering*). Para tal entende-se que as seguintes etapas serão necessárias no trabalho:
1. Seleção de uma amostragem de dados. Propõe-se 1 mês de dados do processo industrial do distribuidor em uma máquina de lingotamento contínuo. 
2. Definição dos sinais para análise das anomalias. Sinais candidatos:
    * Nível de aço no molde
    * Porcentagem de abertura da válvula gaveta
    * Pressão e vazão de Argônio na válvula superior
3. Saneamento dos dados (Tratativa de missing data, erros no sensoriamento, outros).
4. Desenvolvimento de algoritmo de janela deslizante para varredura do sinal e extração de características. Características candidatas:
    * Média, Mínimos e Máximos;
    * Desvio Padrão;
    * Percentil 1 e 99;
    * Coeficiente de Energia.
5. Aplicação do algoritmo de *clustering* **DBCAN** (*Density Based Spatial Clustering of Applications with Noise*). Pretende-se gerar clusters para 2 grupos de variáveis. Um grupo associado ao comportamento de nível do molde e abertura de válvula gaveta e outro associado ao comportamento das variáveis do Argônio.

Será utilizado um pacote Python para extração automática destas características. Referência: [TS-Fresh](https://tsfresh.readthedocs.io/en/latest/text/list_of_features.html) *"Time Series Feature extraction based on scalable hypothesis tests"*

### Resultados Esperados
Grupos representando o comportamento normal serão criados. Pontos que não estão inseridos nos grupos (clusters) que representam as classes “normais” são considerados anômalos e podem indicar uma possível falha no processo. As anomalias identificadas serão cruzadas com informações históricas do processo para validação da eficiência do método. Devido ao grande volume, os dados que estão amostrados em segundos serão representados por janelas de 10 em 10 minutos.

### Bibliografia

1. ESTER, Martin et al. A Density-Based Algorithm for Discovering Clusters in Large Spatial Databases with Noise. In: *2nd International Conference on Knowledge Discovery and Data Mining.* [S.l.: s.n.], 1996. p. 226–231.
2. CHRIST, Maximilian et al. Time Series FeatuRe Extraction on basis of Scalable Hypothesis tests (tsfresh – A Python package). *Neurocomputing*, Elsevier, v. 307, p. 72–77, sep 2018. Disponível em: <<https://www.sciencedirect.com/science/article/pii/S0925231218304843>>.

