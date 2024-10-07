# Fruit Detection

Este repositório contém um projeto de detecção de frutas utilizando uma Rede Neural Convolucional (CNN) para classificar imagens de frutas como saudáveis ou podres. O modelo foi implementado usando TensorFlow/Keras, e também há uma versão utilizando o modelo pré-treinado VGG16.

## Estrutura do Projeto

- `data/`: Contém o diretório `imgs/` com as subpastas para cada classe de fruta (`Apple_Healthy`, `Apple_Rotten`).
- `main.ipynb`: O notebook principal que contém o código para treinar e avaliar o modelo.
- `README.md`: Este arquivo de instruções.

## Requisitos

Certifique-se de ter alguma versão do Python 3.7+ instalada em seu ambiente. O restante das dependências vão ser instaladas automaticamente ao executar o notebook.

## Como Executar o Projeto

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/Guiga-Silva/fruit-detection.git
   ```

2. **Acesse o diretório do projeto:**

   ```bash
   cd fruit-detection
   ```

3. **Estrutura de dados:**

   Coloque suas imagens no diretório `data/imgs` conforme a seguinte estrutura:

   ```
   data/
     imgs/
       Apple_Healthy/
         imagem1.jpg
         imagem2.jpg
         ...
       Apple_Rotten/
         imagem1.jpg
         imagem2.jpg
         ...
   ```

4. **Executar o notebook:**

   Abra e execute o arquivo `fruit_detection.ipynb` em qualquer ambiente compatível com notebooks (como Jupyter ou Google Colab).

5. **Resultados e Avaliação:**

   O notebook vai treinar o modelo, gerar gráficos de acurácia e perda durante o treinamento, além de exibir a matriz de confusão e outras métricas de desempenho como precisão e recall.

## Arquitetura do Modelo CNN

- O modelo CNN contém:
  - 3 camadas de convolução
  - 1 camada densa
  - Regularização com Dropout
  - Otimização com Adam

Além disso, o projeto inclui uma implementação com o modelo pré-treinado **VGG16**, que foi ajustado para o problema de classificação binária.

## Busca por Hiperparâmetros

- O projeto inclui uma busca por hiperparâmetros utilizando **Grid Search** através da biblioteca **Keras Tuner** para otimizar o número de filtros, unidades na camada densa, dropout e taxa de aprendizado.

## Avaliação do Modelo

Após o treinamento, as seguintes métricas são calculadas:

- Acurácia
- Precisão
- Sensibilidade (Recall)
- Matriz de Confusão

## Gráficos e Visualizações

O notebook gera gráficos da perda e acurácia ao longo das épocas, além de exibir uma matriz de confusão para as previsões do modelo.
