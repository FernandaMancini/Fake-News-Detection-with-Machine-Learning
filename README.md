<h1>
     <img align="center" width="60px" src="https://static.vecteezy.com/system/resources/previews/021/432/979/non_2x/fake-news-rubber-stamp-free-png.png">
    <span>Fake News Detection With Machine Learning</span>
</h1>

## ✨ Sobre o Projeto

Em um mundo onde a informação é disseminada em segundos, a identificação de Fake News tornou-se essencial. Este projeto busca solucionar esse problema utilizando Machine Learning e Processamento de Linguagem Natural (NLP) para detectar automaticamente se uma notícia é verdadeira ou falsa. Combinando técnicas como vetorizadores de texto e o modelo probabilístico Naive Bayes, este projeto oferece uma solução de classificação de notícias.

## 📊 Como Funciona?

### 🔬 Vetorizador TF-IDF

TF-IDF (Term Frequency-Inverse Document Frequency) é uma técnica que transforma textos em dados numéricos, avaliando a relevância de cada palavra em relação ao documento e ao corpus completo. Isso ajuda a:

- Diminuir o peso de palavras comuns como "o" ou "e".

- Destacar termos relevantes, como nomes ou tópicos específicos.

No projeto, o TF-IDF:

- Remove palavras irrelevantes (stop words).

- Considera apenas palavras com frequência média no corpus (evitando palavras muito raras ou muito comuns).

### 🧪 Algoritmo Naive Bayes

O Naive Bayes é um classificador probabilístico baseado no Teorema de Bayes. Ele assume que as features (palavras vetorizadas) são independentes entre si, o que o torna simples e eficiente. Por que Naive Bayes?

- Rápido: Ideal para grandes conjuntos de dados textuais.

- Eficiente: Lida bem com problemas de classificação binária (Real x Fake).

- Interpretação: A probabilidade atribuída a cada classe é intuitiva.

No nosso modelo:

- Calculamos a probabilidade de um texto ser "Fake" ou "Real" com base na presença de palavras relevantes.

## 📚 Bibliotecas Utilizadas

<p>
     <img align="center" width="30px" src="https://github.com/user-attachments/assets/e903ba69-63c7-4003-80a2-78c6f75e2e60">
    <span><strong>Pandas</strong></span>
</p>

<p>
     <img align="center" width="30px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/05/Scikit_learn_logo_small.svg/1280px-Scikit_learn_logo_small.svg.png">
    <span><strong> Scikit-learn </strong></span>
</p>
<p>
     <img align="center" width="30px" src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg">
    <span><strong> Datasets </strong></span>
</p>
<p>
     <img align="center" width="30px" src="https://static-00.iconduck.com/assets.00/numpy-icon-1916x2048-tfkpnjo6.png">
    <span><strong>Numpy</strong></span>
</p>

## 🗂️ Dataset
Foi utilizado o dataset do Hugging Face, disponível em: [https://huggingface.co/datasets/ErfanMoosaviMonazzah/fake-news-detection-dataset-English?row=6](https://huggingface.co/datasets/ErfanMoosaviMonazzah/fake-news-detection-dataset-English?row=6)

## Teste em uso: 
Nesta parte, utilizei o título desta notícia do *New York Times* para testar:
https://www.nytimes.com/2025/01/08/world/middleeast/israel-strike-west-bank.html
```
news = ["Israeli Strike in West Bank Kills 3, Including Children"]
news_tfidf = vectorizer.transform(news)
prediction = model.predict(news_tfidf)
print(f"Predição para a notícia: {'Real' if prediction[0] == 1 else 'Fake'}")
```

## Resultados
- **Acurácia:** 92,46%
- **Predição para a Notícia:** Real

## Conclusão
Este projeto demonstra o poder do Machine Learning e do Processamento de Linguagem Natural na solução de problemas complexos como a detecção de Fake News. Embora o modelo tenha mostrado excelente acurácia e métricas, há sempre espaço para melhorias, como a exploração de outros algoritmos. Além disso, pode aparecer erros principalmente considerando a subjetividade das notícias. Por isso, aceito novas sugestões. 

## 🚀 Contribuições
Contribuições são bem-vindas! Caso tenha sugestões ou melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.
