Trabalho Final de Inteligência Artificial
====================================================

Disciplina do Mestrado em Computação Aplicada - IFES (PPCOMP)

## Detecção de anomalias em um sinal temporal de processo industrial utilizando técnica de agrupamento (*Clustering*) 

A proposta deste trabalho é de avaliar umaa série temporal multivariada proveniente de sinais gerados por sensores de um processo industrial de produção de aço, buscando identificar situações anômalas no comportamento destes sinais.  
A abordagem a ser utilizada para identificação será o uso de uma técnica de aprendizado de máquina não supervisionada, neste caso agrupamento (*clustering*). Para tal entende-se que as seguintes etapas serão necessárias no trabalho:

1. Seleção de uma amostragem de dados. Propõe-se 1 mês de dados do processo industrial do distribuidor em uma máquina de lingotamento contínuo. 
2. Definição do sinal para análise das anomalias. Sinais candidato:
* Nível de aço no molde
* Porcentagem de abertura da válvula gaveta
* Pressão e vazão de Argônio na válvula superior
3. Saneamento dos dados (Tratativa de missing data, erros no sensoriamento, outros).
4. Desenvolvimento de algoritmo de janela deslizante para varredura do sinal e extração de características. Características candidatas:
* Média, Mínimos e Máximos;
* Desvio Padrão;
* Percentil 1 e 99;
* Coeficiente de Energia.
Será utilizado um pacote Python para extração automática destas características. Referência: [TS-Fresh](https://tsfresh.readthedocs.io/en/latest/text/list_of_features.html) *"Time Series Feature extraction based on scalable hypothesis tests"*

