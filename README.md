# Classificação de Comandos de Voz com CNN e Espectrogramas

Este projeto implementa um sistema de **classificação de comandos de voz** utilizando **Redes Neurais Convolucionais (CNN)** e técnicas de **Processamento Digital de Sinais (DSP)**, rodando inteiramente no **Google Colab**.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/SEU_LINK_AQUI)

O modelo é treinado para reconhecer comandos como:
- **Abrir**
- **Desligar**
- **Ligar**

---

##  Conceitos Aplicados

O projeto utiliza uma combinação de processamento de áudio e visão computacional:

* **FFT & STFT:** Decomposição do sinal sonoro para análise de frequências.
* **Espectrograma:** Transformação do áudio em uma imagem (mapa de calor de frequências).
* **MFCC:** Coeficientes que capturam as características essenciais da voz.
* **Deep Learning (CNN):** Rede treinada para identificar padrões visuais nos espectrogramas.

---

##  Pipeline do Projeto

1. **Setup:** Instalação de bibliotecas e configuração do ambiente Colab.
2. **Pré-processamento:** Normalização e conversão dos áudios `.wav`.
3. **Extração de Features:** Geração de espectrogramas via `Librosa`.
4. **Modelagem:** Arquitetura CNN construída com `TensorFlow/Keras`.
5. **Predição:** Inferência em tempo real com novos arquivos de áudio.

---

## Tecnologias Utilizadas

* **Ambiente:** Google Colab (Python 3)
* **IA/DL:** TensorFlow / Keras
* **Áudio:** Librosa
* **Gráficos:** Matplotlib
* **Dados:** NumPy & Scikit-learn

---

## Como Executar o Projeto

Para rodar este notebook no Google Colab e testar com seus próprios áudios, siga estas etapas:

### 1. Preparação do Dataset
Baixe a pasta Dataset disponibilizada nesse repositório. A pasta Dataset contem arquivos `.wav` com áudios que eu gravei para usar de amostragem para o treinamento
[Dataset](https://github.com/MoAbner/Classificador-de-Audios/tree/main/Dataset)

### 2. Upload para o Google Drive
Faça o upload da pasta `Dataset` para a raiz do seu **Google Drive**. Isso garante que os arquivos não sejam apagados ao fechar a sessão do Colab.

### 3. Configuração no Colab
Ao abrir o notebook, execute a célula de configuração inicial:
1. Clique no ícone de **Pasta** na barra lateral esquerda.
2. Clique no botão **"Montar Drive"** (ícone de pasta com o logo do Drive).
3. Siga as instruções na tela para permitir o acesso.

### 4. Ajuste de Caminhos
No código, certifique-se de que a variável de caminho aponta para o local correto no seu Drive:
```python
PATH_DATASET = '/content/drive/MyDrive/Dataset/Audios'
--- 
```
 ### 5. Analise de seus Áudios (Ligar, Desligar ou Abrir) 
 Se quiser analisar algum áudio diferente dos que estão na pasta testes basta fazer o upload do arquivo do áudio em `.wav` na pasta Testes, Copie seu caminho e coloque dentro dos parametros que chama a função na seção de testes.
 Se ao gravar seu arquivo é de um formato diferente de `.wav`, Siga esses passos:
 1. Converta ele para `.wav`, Existem sites que convertem gratuitamente, eu recomendo o HappyScribe: https://www.happyscribe.com/pt
 2. Adicione seu arquivo em `.wav` na pasta de testes
 3. Copie seu caminho, e coloque dentro dos parametros que chama a função na seção de testes

 ### 6. Rodando o código no Colab
 Execute as células sequencialmente (`Shift + Enter`).
 
## Estrutura de Pastas (Ambiente Colab)
```
/content/ 
└── Dataset/                    # Pasta principal de dados
    ├── Audios/                 # Dados de Treino
    │   ├── abrir/              # Pastas de classes (Abrir)
    │   ├── desligar/           # Pastas de classes (Desligar)
    │   └── ligar/              # Pastas de classes (Ligar)
    │
    └── testes/                 # Pasta que armazena os áudios para a análise

```
## Motivação e Considerações Finais

Este projeto nasceu do desejo de explorar a interseção entre o **Processamento Digital de Sinais (DSP)** e a **Inteligência Artificial**. A voz é uma das formas mais naturais de interface humano-computador, e entender como transformar ondas sonoras em dados que uma rede neural pode "enxergar" (através de espectrogramas) foi o grande desafio técnico aqui.

A principal motivação foi aplicar conceitos teóricos de redes neurais convolucionais (CNN) em um problema cotidiano: a automação por comandos de voz.

Este projeto foi criado baseado em meu estudo sobre processamento digital de sinais usando Python e informações que obtive no grupo de estudo sobre visão computacional onde discutimos como diferentes tipos de dados podem ser processados por redes neurais.

Se você tem interesse em tecnologia, IA e Visão computacional e quer participar e contribuir para nossa comunidade entre no nosso grupo de estudos no whatssapp.

Grupo de Estudos Visão Computacional: https://chat.whatsapp.com/G5lLNJdp9oxDb0fZVIT4ca?mode=ems_copy_c.

