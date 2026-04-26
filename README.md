# Aula Prática 4: DFT e DCT 

[cite_start]Este repositório contém o desenvolvimento da **Aula Prática 4** da disciplina de **Processamento de Sinais I**, ministrada pelo professor **Rafael Chaves**[cite: 1, 2, 3]. [cite_start]O objetivo é explorar as propriedades e aplicações da Transformada Discreta de Fourier (DFT) e da Transformada de Cosseno Discreta (DCT) em sinais e imagens[cite: 3].

---

## 🎯 Objetivos da Prática

* [cite_start]Analisar as diferenças fundamentais entre a DFT e a DTFT[cite: 4, 5].
* [cite_start]Estudar o impacto do tamanho da transformada na resolução espectral e os efeitos do *zero-padding*[cite: 8, 9, 16].
* [cite_start]Avaliar o desempenho da DFT e DCT na compressão de sinais de áudio (1-D)[cite: 18, 19, 20].
* [cite_start]Implementar e analisar a compressão de imagens (2-D) utilizando a DCT em blocos, simulando o padrão JPEG[cite: 24, 26, 28].

---

## 🛠️ Conteúdo das Atividades

### 1. Comparação DFT vs. DTFT
[cite_start]Análise da DFT como a versão discreta da DTFT, representando amplitude e fase de componentes frequenciais em sequências finitas[cite: 4].
* [cite_start]**Sinal Analisado:** $x[n]=\delta[n]-\delta[n-1]+\delta[n-2]-\delta[n-3]$[cite: 6].
* [cite_start]**Experimento:** Comparação visual entre a DTFT e a DFT para comprimentos $N \in \{4, 16, 64, 1024\}$[cite: 7].

### 2. Resolução Espectral e Zero-Padding
[cite_start]Estudo de como o número de amostras reais versus a adição de zeros influencia a identificação de componentes de frequência próximas[cite: 8, 13].
* [cite_start]**Sinal:** $x(t)=\sin(2\pi t)+\sin(2,2\pi t)$ amostrado a $f_{s}=10$ Hz[cite: 10, 11].
* [cite_start]**Testes Realizados:** * DFT com 64 amostras originais[cite: 12].
    * [cite_start]DFT de 128 pontos com *zero-padding* (64 zeros)[cite: 13].
    * [cite_start]DFT com 128 amostras reais (sem *zero-padding*)[cite: 14].
    * [cite_start]Investigação de aumentos adicionais com 128 e 384 zeros[cite: 15].

### 3. Compressão de Áudio (1-D)
[cite_start]Comparação entre DFT e DCT para compressão do sinal `handel.wav`[cite: 20].
* [cite_start]**Fatores de Retenção de Energia:** $99.5\%$, $99.0\%$, $90.0\%$, $75.0\%$ e $50.0\%$[cite: 20].
* [cite_start]**Métricas de Avaliação:** Erro Quadrático Médio (MSE), quantidade de coeficientes necessários e análise subjetiva da qualidade sonora[cite: 22, 23].

### 4. Análise e Compressão de Imagem (2-D)
[cite_start]Uso da DCT para analisar a concentração de energia na imagem `sosias.jpg`[cite: 25].
* [cite_start]**Compressão por Blocos:** Implementação de compressão em blocos de $L \times L$ para evitar degradação excessiva[cite: 27, 28].
* [cite_start]**Parâmetros de Teste:** * Tamanhos de bloco: $L \in \{8, 64\}$[cite: 28].
    * [cite_start]Fatores de compressão: $r \in \{95\%, 50\%\}$[cite: 28].
* [cite_start]**Avaliação:** Comparação do MSE em relação à taxa de compressão e ao tamanho do bloco[cite: 31].

---

## 📊 Comparativo Teórico

| Característica | DFT | DCT |
| :--- | :--- | :--- |
| **Componentes** | [cite_start]Senos e Cossenos (Complexo) [cite: 4] | [cite_start]Apenas Cossenos (Real) [cite: 19] |
| **Aplicação Principal** | [cite_start]Análise Espectral Geral [cite: 3] | [cite_start]Compressão de Dados (Áudio/Imagem) [cite: 19, 24] |
| **Concentração de Energia** | Moderada | [cite_start]Alta (Excelente para compressão) [cite: 27] |

---

## 💻 Requisitos
* Ambiente de simulação (Python, MATLAB ou Octave).
* Arquivos de mídia: `handel.wav` e `sosias.jpg`.

---
*Este material faz parte das atividades práticas da disciplina de Processamento de Sinais I.*
