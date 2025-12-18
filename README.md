# Hackathon ONE G8 — Sentiment Analysis API


Projeto de **análise de sentimentos** (Positivo, Negativo e Neutro) desenvolvido em **Python**, utilizando **Scikit-Learn** com pipeline **TF-IDF + Regressão Logística**, com forte foco em **confiabilidade, robustez frente à linguagem informal e explicabilidade das predições**.


Este projeto foi evoluído a partir de testes extensivos com **avaliações reais**, incluindo frases ambíguas, negativas implícitas e construções informais comuns em feedbacks de usuários.


---


## 📂 Estrutura do Projeto


- **app.py** — API Flask (versão final será integrada ao backend).
- **modelo_lr_sentimentos.pkl** — Modelo de Regressão Logística treinado.
- **modelo_svm_sentimentos.pkl** — Modelo SVM Linear treinado para comparação.
- **tfidf.pkl** — Vetorizador TF-IDF persistido.
- **Data.csv** — Dataset base + dados incrementais (incluindo frases ambíguas).
- **notebooks/** — Análises exploratórias, testes, validações e prototipação.
- **requirements.txt** — Dependências do projeto.


---


## 🚀 Funcionalidades


- Limpeza e normalização avançada de texto.
- Tratamento de **negações** e **intensificadores** no pré-processamento.
- Balanceamento das classes com **Random Oversampling** (aplicado apenas no treino).
- Classificação de sentimentos em **3 categorias**: Positivo, Negativo e Neutro.
- Avaliação com métricas confiáveis:
- Acurácia
- Precision, Recall e F1-score
- Matrizes de confusão (absoluta e normalizada)
- Validação cruzada estratificada (F1 Macro).
- Predição com **probabilidade associada**.
- **Explicabilidade por instância**, retornando:
- Palavras mais influentes
- Peso de contribuição de cada termo
- Exportação do modelo e do TF-IDF com **joblib** para uso em produção.
- API de predição via endpoint **POST /predict**.


---


## 🧠 Estratégia de Confiabilidade


Durante os testes, identificou-se um padrão recorrente de erro em frases:
- com **advérbios de intensidade** (ex: "muito")
- combinados com **negações ou avaliações negativas implícitas**


Em vez de aplicar regras rígidas ou heurísticas artificiais, a confiabilidade do modelo foi aprimorada através de:


- **Enriquecimento do dataset** com avaliações reais e ambíguas
- Inclusão intencional de frases semanticamente negativas, porém linguisticamente confusas
- Re-treinamento do modelo mantendo o pipeline original


Essa abordagem reduziu significativamente falsos positivos e tornou o modelo mais robusto frente ao uso informal da linguagem, cenário comum em avaliações de usuários.


---


## 📌 Status do Projeto


✔ Pipeline de Machine Learning **consolidado e validado**


✔ Modelo aprovado para uso em ambiente controlado ou MVP


✔ Alta interpretabilidade e rastreabilidade das decisões
---


## 🏁 Observação Final


Este projeto prioriza **qualidade semântica**, **decisões explicáveis** e **aderência à linguagem real do usuário**, aceitando que ambiguidades fazem parte do domínio do problema.


Um pequeno número residual de falsos positivos é tratado como limite estatístico natural do contexto mitigado via análise de confiança.
