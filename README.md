# Hackathon ONE G8 — Sentiment Analysis API

Projeto de análise de sentimentos (Positivo, Negativo e Neutro) desenvolvido em Python, utilizando Scikit-Learn com pipeline TF-IDF + Regressão Logística, focado em acurácia, confiabilidade e explicabilidade das predições.

## 📂 Estrutura do Projeto

* `app.py` — API Flask (versão final será integrada ao backend).
* `sentiment_pipeline.joblib` — Modelo treinado.
* `label_encoder.joblib` — Codificador das classes.
* `Data.csv` — Dataset original.
* `notebooks/` — Testes, análises e prototipação.
* `requirements.txt` — Dependências do projeto.

## 🚀 Funcionalidades

* Limpeza e normalização de texto.

* Balanceamento das classes com Random Oversampling (ênfase na classe Neutra).

* Classificação de sentimentos em 3 categorias.

* Validação com métricas detalhadas e matrizes de confusão normalizadas.

* Predição com probabilidade associada.

* Explicabilidade por instância, retornando as palavras mais influentes e seus pesos.

* Exportação do modelo e do TF-IDF com joblib para uso em produção.

* API de predição via endpoint POST /predict.


## 📌 Status

Projeto em fase de estruturação e testes. Novos módulos e ajustes ainda serão adicionados.

