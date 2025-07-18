
# HR Analytics Challenge - Machine Learning para Previsão de Attrition

## 📌 Visão Geral do Projeto
Solução preditiva para reduzir em 20-30% a taxa de attrition na TechCorp Brasil, com economia estimada de R$ 9-13,5 milhões/ano.

**Desafio Empresarial**:  
35% de rotatividade voluntária em 12 meses (R$ 45 milhões em custos)

## 🛠️ Tecnologias Utilizadas
- **Linguagem**: Python 3.10+
- **Principais Bibliotecas**: python, pandas, numpy, scikit-learn, xgboost, catboost, shap, matplotlib
- **Ferramentas**: Jupyter Notebook, Git, VS Code

📊 Métricas dos Modelos
| Modelo               | Acurácia | Precisão | Recall | F1-Score | AUC-ROC |
|----------------------|----------|----------|--------|----------|---------|
| LogisticRegression   | 76%      | 36%      | 66%    | 0.46     | 0.80    |
| RandomForest         | 84%      | 46%      | 13%    | 0.20     | 0.81    |
| XGBoost              | 87%      | 72%      | 28%    | 0.40     | 0.77    |
| CatBoost             | 78%      | 36%      | 53%    | 0.43     | 0.78    |

🔍 Variáveis Mais Relevantes (SHAP)
- **StagnationRisk** (22% impacto)
- **OverTime_Binary** (3× maior risco)
- **SalaryRatio** (+18% risco)

🚀 Como Executar
Clone o repositório:

bash
git clone https://github.com/seu-usuario/hr-analytics-challenge.git
Instale as dependências:

bash
pip install -r requirements.txt
Execute o pipeline completo:

bash
python src/main_pipeline.py
🗂️ Estrutura do Projeto
text
hr-analytics/
├── data/
│   ├── raw/            # Dados brutos
│   └── processed/      # Dados tratados
├── notebooks/
│   ├── 1_EDA.ipynb
│   ├── 2_Modelagem.ipynb
│   └── 3_Resultados.ipynb
├── src/
│   ├── preprocessing.py
│   ├── train_model.py
│   └── visualize.py
├── README.md
└── requirements.txt
📌 Principais Insights
python
# Exemplo de insight acionável
high_risk = df[(df['StagnationRisk'] > 15) & 
               (df['SalaryRatio'] < 0.8)]
print(f"{len(high_risk)} funcionários com 83% de risco de atrito")
📅 Próximos Passos
Implementar dashboard Power BI/Tableau

Testar técnicas avançadas de balanceamento

Integrar com sistema de RH via API

👥 Equipe
Nome	RA	Função
Fábio Silva de Medeiros	10734804	Análise de Dados
Samuel Batista de Oliveira	10738597	Modelagem Preditiva
Marcus Moreira	10734633	Engenharia de Features
Jackson Ventura	10737764	Visualização
