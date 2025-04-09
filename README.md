# 🛒 Predição de Preços no Varejo Online com Machine Learning

Este projeto tem como objetivo aplicar técnicas de aprendizado de máquina para prever o preço unitário de produtos a partir do conjunto de dados **Online Retail**. A solução engloba pré-processamento dos dados, análise exploratória, balanceamento utilizando a técnica `NearMiss` e avaliação de modelos de regressão, com foco em transformações, engenharia de atributos e validação estatística.

---

## 📁 Estrutura Geral do Projeto

- **Pré-processamento e Limpeza dos Dados**
  Remoção de valores nulos, tratamento de outliers e conversão de tipos.

- **Análise Exploratória (EDA)**
  Visualizações com gráficos de dispersão, boxplots, histogramas e análise de variáveis temporais para identificar padrões de consumo e comportamento.

- **Engenharia de Atributos**
  Criação de variáveis derivadas: Mês, Dia da Semana, Turno do Dia, e categorização de preços em faixas (`Low`, `Average`, `High`).

- **Balanceamento das Classes**
  Utilização do algoritmo `NearMiss` para equilibrar a distribuição entre as categorias de preços.

- **Preparação dos Dados**
  One-hot encoding de variáveis categóricas e normalização com `MinMaxScaler`.

- **Modelagem Preditiva**
  Avaliação dos seguintes modelos de regressão:
  - K-Nearest Neighbors Regressor
  - Decision Tree Regressor
  - Random Forest Regressor
  - Linear Regression

- **Validação Cruzada e Tunagem de Hiperparâmetros**
  Uso de `KFold` e `ParameterGrid` para otimizar e avaliar o desempenho dos modelos.

- **Comparação Estatística**
  Teste de Wilcoxon para comparar estatisticamente a performance dos modelos.

---

## 📊 Dataset

- **Nome**: Online Retail
- **Fonte**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Descrição**:
  - Contém transações ocorridas entre dezembro de 2010 e dezembro de 2011.
  - Abrange informações sobre produtos, preços, datas, localização dos clientes e quantidade de itens comprados.
- **Principais Colunas**:
  - `InvoiceNo`
  - `StockCode`
  - `Description`
  - `Quantity`
  - `InvoiceDate`
  - `UnitPrice`
  - `CustomerID`
  - `Country`

---

## ⚙️ Modelos de Machine Learning Avaliados

| Modelo                   | Estratégia de Tunagem              | Métrica Avaliada         |
|--------------------------|------------------------------------|--------------------------|
| **KNeighborsRegressor**  | `n_neighbors` e `metric`           | `mean_squared_error`     |
| **DecisionTreeRegressor**| `max_depth`                        | `mean_squared_error`     |
| **RandomForestRegressor**| `n_estimators`, `max_depth`         | `mean_squared_error`     |
| **LinearRegression**     | Sem tunagem                        | `mean_squared_error`     |

Os modelos foram avaliados utilizando 10 folds de validação cruzada e os resultados indicaram que o **Random Forest** obteve o menor erro médio quadrático, demonstrando melhor performance na previsão do preço unitário.

---

## 📈 Resultados

- **Validação Cruzada**: Cada modelo foi treinado e avaliado em 10 folds, garantindo robustez no desempenho.
- **Teste Estatístico**: O teste de Wilcoxon confirmou diferenças estatisticamente significativas entre os modelos, evidenciando a superioridade do Random Forest na maioria das comparações.

---

## ▶️ Como Executar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/pkziinn10/Machine_Learning.git
   cd Machine_Learning

2. **Crie um ambiente virtual**:

```bash
   python -m venv venv
```
📌 Linux/macOS
```bash
  source venv/bin/activate
```
📌 Windows
```bash
  venv\Scripts\activate
```

3. **Instale os pacotes**:
```bash
  pip install -r requirements.txt
```
4.**Execute o notebook ou script principal**:
  `main.ipynb` ou `main.py`

## 📊 Dataset

- Nome: Online Retail

- Fonte: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)

- Descrição:

Contém transações entre dezembro de 2010 e dezembro de 2011.

Informações sobre produtos, preços, datas, localização dos clientes e comportamento de compra.

Principais colunas:

InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

## ✅ Conclusão

- Este projeto demonstra como transformar um conjunto de dados com forte desbalanceamento em um problema de regressão eficiente e confiável. O uso de técnicas como:

- Engenharia de atributos,

- Balanceamento com NearMiss,

- Modelos como Random Forest,

- Validação cruzada com K-Fold,

- Testes estatísticos (Wilcoxon),

- garantiu resultados mais robustos e generalizáveis. O Random Forest foi o modelo com melhor desempenho e significância estatística.

## 📫 Contato

- Caso tenha dúvidas ou queira trocar ideias:

- 📧 Email: pedrinhokauan824@gmail.com

- 💼 LinkedIn: www.linkedin.com/in/pkziinn10

- 💻 GitHub: @pkziinn10
