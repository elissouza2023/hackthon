# Hackathon ONE G8 — Sentiment Analysis API

Projeto em desenvolvimento para análise de sentimentos (Positivo, Negativo e Neutro) utilizando **Python**, **Scikit-Learn** e **Pipeline TF-IDF + Regressão Logística**.

## 📂 Estrutura do Projeto

* `app.py` — API Flask (versão final será integrada ao backend).
* `sentiment_pipeline.joblib` — Modelo treinado.
* `label_encoder.joblib` — Codificador das classes.
* `Praticas ESG em T.I.csv` — Dataset original.
* `notebooks/` — Testes, análises e prototipação.
* `requirements.txt` — Dependências do projeto.

## 🚀 Funcionalidades

* Treinamento do modelo com limpeza de texto.
* Balanceamento usando **Random Oversampling**.
* Classificação em 3 categorias.
* API de predição via método `POST /predict`.


## 📌 Status

Projeto em fase de estruturação e testes. Novos módulos e ajustes ainda serão adicionados.

