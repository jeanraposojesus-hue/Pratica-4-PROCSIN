# Aula Prática 4: DFT e DCT 

[cite_start]Este repositório contém o desenvolvimento da **Aula Prática 4** da disciplina de **Processamento de Sinais I**, ministrada pelo professor **Rafael Chaves**[cite: 1, 2]. [cite_start]O foco é a aplicação da Transformada Discreta de Fourier (DFT) e da Transformada de Cosseno Discreta (DCT) para análise e compressão de sinais[cite: 3].

---

## 🎯 Objetivos da Prática

* [cite_start]**DFT vs. DTFT:** Analisar a DFT como a versão discreta da DTFT, convertendo sequências finitas em componentes de amplitude e fase[cite: 4].
* [cite_start]**Resolução Espectral:** Avaliar como o tamanho da transformada e o uso de *zero-padding* afetam a distinção de frequências próximas[cite: 8, 9].
* [cite_start]**Compressão 1-D:** Comparar o desempenho da DFT e DCT na compressão de áudio[cite: 18, 19].
* [cite_start]**Compressão 2-D:** Aplicar a DCT para compressão de imagens em blocos, simulando o padrão JPEG[cite: 24, 28].

---

## 🛠️ Atividades Desenvolvidas

### 1. Análise de Frequência
[cite_start]Comparação entre a DTFT e a DFT para diferentes valores de $N \in \{4, 16, 64, 1024\}$[cite: 7], utilizando o sinal:
[cite_start]$x[n]=\delta[n]-\delta[n-1]+\delta[n-2]-\delta[n-3]$ [cite: 6]

### 2. Resolução e Zero-Padding
Estudo do impacto da amostragem e do preenchimento com zeros no sinal:
[cite_start]$x(t)=\sin(2\pi t)+\sin(2,2\pi t)$ com $f_{s}=10$ Hz [cite: 10, 11]
* [cite_start]Foram analisados casos com 64 amostras, 128 amostras reais e variações com *zero-padding* de até 384 zeros[cite: 12, 13, 14, 15].

### 3. Compressão de Áudio (Sinais 1-D)
[cite_start]Compressão do arquivo `handel.wav` para fatores de retenção de energia de $99.5\%$, $99.0\%$, $90.0\%$, $75.0\%$ e $50.0\%$[cite: 20].
* [cite_start]**Métricas:** Quantidade de coeficientes e Erro Quadrático Médio (MSE)[cite: 23].

### 4. Compressão de Imagem (Sinais 2-D)
[cite_start]Análise e compressão da imagem `sosias.jpg` utilizando a DCT em blocos de $L \times L$[cite: 24, 25, 28].
* [cite_start]**Blocos:** $L=8$ e $L=64$[cite: 28].
* [cite_start]**Fatores de Compressão:** $95\%$ e $50\%$[cite: 28].

---

## 📊 Conclusões Sugeridas
* [cite_start]A resolução da DFT depende diretamente do tamanho real da amostra; o *zero-padding* apenas interpola o espectro, não criando nova resolução[cite: 16].
* [cite_start]A DCT geralmente apresenta melhor concentração de energia que a DFT para compressão de sinais reais[cite: 27].

---
*Relatório de aula prática - Engenharia de Processamento de Sinais.*
