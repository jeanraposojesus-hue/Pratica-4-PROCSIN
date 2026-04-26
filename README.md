# Aula Prática 4: DFT e DCT 

Este repositório contém o desenvolvimento da **Aula Prática 4** da disciplina de **Processamento de Sinais I**, ministrada pelo professor **Rafael Chaves**. O objetivo é explorar as propriedades e aplicações da Transformada Discreta de Fourier (DFT) e da Transformada de Cosseno Discreta (DCT) em sinais e imagens.

---

## 🎯 Objetivos da Prática

* Analisar as diferenças fundamentais entre a DFT e a DTFT.
* Estudar o impacto do tamanho da transformada na resolução espectral e os efeitos do *zero-padding*.
* Avaliar o desempenho da DFT e DCT na compressão de sinais de áudio (1-D).
* Implementar e analisar a compressão de imagens (2-D) utilizando a DCT em blocos, simulando o padrão JPEG.

---

## 🛠️ Conteúdo das Atividades

### 1. Comparação DFT vs. DTFT
Análise da DFT como a versão discreta da DTFT, representando amplitude e fase de componentes frequenciais em sequências finitas.
* **Sinal Analisado:** $x[n]=\delta[n]-\delta[n-1]+\delta[n-2]-\delta[n-3]$.
* **Experimento:** Comparação visual entre a DTFT e a DFT para comprimentos $N \in \{4, 16, 64, 1024\}$.

### 2. Resolução Espectral e Zero-Padding
Estudo de como o número de amostras reais versus a adição de zeros influencia a identificação de componentes de frequência próximas.
* **Sinal:** $x(t)=\sin(2\pi t)+\sin(2,2\pi t)$ amostrado a $f_{s}=10$ Hz.
* **Testes Realizados:** * DFT com 64 amostras originais.
    * DFT de 128 pontos com
