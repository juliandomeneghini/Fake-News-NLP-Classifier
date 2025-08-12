# 📰 Classificação de Fake News - NLP  
**RU:** 4061848  
**Disciplina:** Processamento de Linguagem Natural (NLP)  
**Objetivo:** Treinar um modelo de aprendizado de máquina capaz de classificar notícias como **VERDADEIRAS** ou **FALSAS** utilizando o corpus Fake.br-Corpus.

---

## 📋 Descrição do Projeto  
Este projeto implementa uma solução de **classificação binária** para identificar fake news em português.  
A abordagem segue as etapas clássicas de **aquisição de dados, pré-processamento, modelagem e representação**.

O corpus utilizado é o **[Fake.br-Corpus](https://github.com/roneysco/Fake.br-Corpus)**, já pré-processado, com remoção de HTML, links e normalização básica.

O código foi **adaptado** a partir do repositório oficial da disciplina:  
📌 [https://github.com/N-CPUninter/NLP](https://github.com/N-CPUninter/NLP)  

Além disso, são geradas **nuvens de palavras** para visualizar os termos mais relevantes na classificação de notícias verdadeiras e falsas.

---

## 🛠️ Tecnologias Utilizadas  
- **Python 3.x**  
- **Bibliotecas principais:**
  - `pandas` (manipulação de dados)
  - `nltk` (pré-processamento de texto)
  - `scikit-learn` (vetorização e modelagem)
  - `wordcloud` (geração de nuvens de palavras)
  - `matplotlib` (visualização)
  - `numpy` (operações matemáticas)
- **Modelo:** Regressão Logística (`LogisticRegression`)

---

## 📂 Estrutura do Código  
O código está dividido em quatro etapas principais:

1. **Instalação e Importação de Bibliotecas**  
   - Baixa o dataset pré-processado.  
   - Clona scripts auxiliares do repositório de apoio.  

2. **Aquisição e Estruturação dos Dados**  
   - Leitura do `pre-processed.csv`.  
   - Remoção de valores nulos.  

3. **Pré-Processamento dos Textos**  
   - Tokenização  
   - Conversão para minúsculas  
   - Remoção de acentos, números, pontuações e stopwords  
   - Stemming (radicalização) com `RSLPStemmer`  
   - Truncamento para normalização do tamanho dos textos  
   - Reconstrução dos textos para vetorização  

4. **Mineração e Modelagem**  
   - Vetorização TF-IDF com n-gramas (1 a 3)  
   - Treinamento da Regressão Logística  
   - Avaliação da acurácia  

5. **Representação e Respostas**  
   - Extração dos termos mais relevantes para cada classe  
   - Geração de nuvens de palavras com máscaras (`thumbs_up` e `thumbs_down`)  

---

## 📊 Resultados Obtidos  
- **Acurácia final:** ~89,6%  
- **Quantidade de termos para identificar notícias verdadeiras:** *depende da execução*  
- **Quantidade de termos para identificar notícias falsas:** *depende da execução*  

---

## 🚀 Como Executar no Google Colab  
1. Abra o Google Colab: [https://colab.research.google.com/](https://colab.research.google.com/)  
2. Crie um novo notebook.  
3. Copie e cole o código principal do repositório.  
4. Execute as células na ordem.

---

## 🖼️ Exemplos de Saída  

### 🔵 Nuvem de Palavras - Notícias Verdadeiras  
![Nuvem de Palavras Verdadeiras](nuvem_verdadeiras.png)

### 🔴 Nuvem de Palavras - Notícias Falsas  
![Nuvem de Palavras Falsas](nuvem_falsas.png)

---

## 📚 Referências  
- [Fake.br-Corpus](https://github.com/roneysco/Fake.br-Corpus)  
- [Repositório base da disciplina - N-CPUninter/NLP](https://github.com/N-CPUninter/NLP)  
- [Documentação NLTK](https://www.nltk.org/)  
- [Documentação Scikit-learn](https://scikit-learn.org/)  

---
