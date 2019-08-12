Trabalho Final de Inteligência Artificial
====================================================

Disciplina do Mestrado em Computação Aplicada - IFES (PPCOMP)

## Detecção de anomalias em um sinal temporal de processo industrial utilizando técnica de agrupamento (*Clustering*) 

A proposta deste trabalho é de avaliar uma série temporal univariada proveniente de um sinal gerado por um sensor de um processo industrial de produção de aço, buscando identificar situações anômalas no comportamento deste sinal.  
A abordagem a ser utilizada para identificação será o uso de uma técnica de aprendizado de máquina não supervisionada, neste caso agrupamento (*clustering*). Para tal entende-se que as seguintes etapas serão necessárias no trabalho:

1. Seleção de uma amostragem de dados. Propõe-se 1 mês de dados do processo industrial do distribuidor em uma máquina de lingotamento contínuo. 
2. Definição do sinal para análise das anomalias. Sinais candidatos
a.	Nível de aço no molde
b.	Porcentagem de abertura da válvula gaveta 
3. Saneamento dos dados (Tratativa de missing data, erros no sensoriamento, outros).
4. Desenvolvimento de algoritmo de janela deslizante para varredura do sinal e extração de características. Características candidatas:

