# Localização de Usuários em Redes Celulares

Este repositório contém a solução desenvolvida para o projeto da disciplina **Comunicações Móveis 2024.2**. O objetivo do projeto é estimar a localização de usuários móveis em redes celulares utilizando diversas abordagens de aprendizado de máquina e técnicas de geração de dados.

---

## Equipe 3
- Anne Collier
- Bárbara Vaz
- Lívia Bion
- Pedro Cecílio

---

## Visão Geral do Projeto

Esta solução aborda o problema de localização utilizando os seguintes métodos:

- **Fingerprinting (com kNN):**  
  Aproximação baseada em "radio map", onde as medições de RSSI e delays são utilizadas como assinaturas digitais para comparar com pontos de referência.

- **Random Forest:**  
  Utilização de um ensemble de árvores de decisão para prever a posição (latitude e longitude) com base nos sinais medidos.

- **XGBoost:**  
  Aplicação de boosting para regressão, com ajuste de hiperparâmetros e validação via cross-validation, visando melhorar a acurácia na predição das posições.

- **Geração de Dados Sintéticos com GAN:**  
  Uso de Redes Adversariais Generativas (GAN) para expandir a base de dados original, gerando amostras sintéticas que auxiliam na robustez e generalização dos modelos.

Cada método foi testado tanto com a base de dados original quanto com a base ampliada com dados sintéticos. Ao final, uma comparação geral dos métodos foi realizada (apresentada em uma apresentação e relatório, que não estão incluídos neste repositório).

---

## Estrutura do Repositório

- `requirements.txt`  
  Lista de dependências e bibliotecas necessárias para executar os notebooks e scripts do projeto.

- Notebooks:
  - `fingerprint-method.ipynb`  
    Implementação do método de fingerprinting utilizando kNN.
  - `RandomFlorest_Final.ipynb` e `RandomFlorest_Final_dados_sinteticos.ipynb`  
    Implementação e avaliação do modelo Random Florest.
  - `XGBoostComMovNatural.ipynb`  
    Implementação e ajuste do modelo XGBoost.
  - `GANComMov.ipynb`  
    Implementação da geração de dados sintéticos com GAN.
- Dados:
  - Arquivos CSV contendo as bases de treinamento, teste e resultados de cada método.

---

## Requisitos e Configuração

### Pré-requisitos
- Python 3.x
- Bibliotecas Python listadas em `requirements.txt`

### Instalação

1. Clone o repositório:
   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_REPOSITORIO>
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
