# Machine-Learning-Aplicado-HR-Analytics-Challenge
HR Analytics Challenge - Machine Learning para Previsão de Atrito (Attrition)
Visão Geral do Projeto
Este projeto visa desenvolver um modelo preditivo de machine learning para ajudar a TechCorp Brasil a abordar sua alta taxa de atrito de funcionários (35% em 12 meses), que resultou em perdas financeiras significativas (R$ 45 milhões anualmente). Nossa solução combina análise exploratória de dados, algoritmos avançados como XGBoost e interpretação SHAP para identificar funcionários em risco com até 6 meses de antecedência.

Principais Características
Modelagem Preditiva: Utiliza XGBoost, Random Forest e Regressão Logística para prever risco de atrito

Variáveis Críticas Identificadas: Hora Extra, Tempo na Empresa, Satisfação no Trabalho, Equilíbrio Vida-Trabalho, Relação com o Gestor

Interpretabilidade: Valores SHAP explicam as previsões do modelo

Recomendações Estratégicas: Insights acionáveis para intervenções de RH

Membros da Equipe
Fábio Silva de Medeiros (RA 10734804)

Samuel Batista de Oliveira (RA 10738597)

Marcus Moreira (RA 10734633)

Jackson Ventura (RA 10737764)

Metodologia
Análise Exploratória de Dados (EDA)

Estatísticas descritivas e identificação de padrões

Detecção de outliers usando método IQR

Análise de correlação entre variáveis

Engenharia de Features

Criação de novas métricas:

Razão Salarial: Salário atual vs. média do cargo

Índice de Crescimento: Tempo na empresa vs. número de promoções

Risco de Estagnação: Anos desde última promoção × nível hierárquico

Desenvolvimento do Modelo

Teste de quatro algoritmos:

Regressão Logística

Random Forest

XGBoost

CatBoost

Otimização usando GridSearchCV com validação cruzada de 5 folds

Foco em F1-Score e AUC-PR para dados desbalanceados

Avaliação do Modelo

Métricas-chave: Precisão, Recall, F1-Score, AUC-ROC

Valores SHAP para interpretação da importância das variáveis

Resultados
Modelo	Acurácia	Precisão (Classe 1)	Recall (Classe 1)	F1-Score (Classe 1)	AUC-ROC
LogisticRegression	76%	36%	66%	0.46	0.80
RandomForest	84%	46%	13%	0.20	0.81
XGBoost	87%	72%	28%	0.40	0.77
CatBoost	78%	36%	53%	0.43	0.78
Variáveis Mais Preditivas:

Risco de Estagnação (22% de contribuição para o risco de atrito)

Hora Extra Binária (3x maior risco para funcionários com horas extras)

Razão Salarial (18% aumento de risco para salários abaixo da média)

Impacto nos Negócios
Resultados Esperados:

Redução de 20-30% no atrito no primeiro ano

Economia estimada de R$ 9-13,5 milhões

Recomendações Estratégicas:

Planos de retenção personalizados (ajustes de carga horária, mentorias)

Programas de desenvolvimento de carreira para funcionários estagnados

Revisões salariais para funcionários de alto risco

Monitoramento contínuo com atualizações trimestrais do modelo

Estrutura do Repositório
text
HR-Analytics-Challenge/
├── data/                    # Dados brutos e processados
├── notebooks/               # Jupyter notebooks com análises
│   ├── EDA.ipynb            # Análise Exploratória de Dados
│   ├── Feature_Engineering.ipynb
│   ├── Model_Training.ipynb
│   └── Model_Evaluation.ipynb
├── src/                     # Código fonte
│   ├── preprocessing.py     # Limpeza de dados e engenharia de features
│   ├── models.py            # Funções de treinamento de modelos
│   └── visualization.py     # Funções de visualização
├── reports/                 # Relatórios e visualizações geradas
├── README.md                # Este arquivo
└── requirements.txt         # Dependências Python
Como Começar
Clone o repositório:

bash
git clone https://github.com/seuusuario/HR-Analytics-Challenge.git
cd HR-Analytics-Challenge
Instale as dependências:

bash
pip install -r requirements.txt
Execute os Jupyter notebooks no diretório notebooks/ para reproduzir a análise.

Dependências
Python 3.8+

pandas

numpy

scikit-learn

xgboost

catboost

shap

matplotlib

seaborn

imbalanced-learn

Trabalhos Futuros
Implementar SMOTE para melhor tratamento de dados desbalanceados

Desenvolver um painel interativo para equipes de RH

Expandir o conjunto de variáveis com dados adicionais de funcionários

Implementar sistema de monitoramento do modelo para acompanhamento de desempenho

Licença
Este projeto está licenciado sob a Licença MIT - consulte o arquivo LICENSE para obter detalhes.

Para quaisquer dúvidas, entre em contato com os membros da equipe do projeto.


