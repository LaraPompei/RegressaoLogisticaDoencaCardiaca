# Projeto de Doenças Cardiovasculares com Regressão Logística

Este projeto tem como objetivo construir um modelo de classificação para prever a presença de doença cardiovascular a partir de dados reais de pacientes. O trabalho inclui tratamento da base, análise exploratória, engenharia de variáveis, separação treino e teste, padronização de variáveis contínuas e treinamento de um modelo de Regressão Logística.

## Objetivo
Prever a variável alvo `cardio_disease`, onde:
* 1 indica que o paciente tem doença cardiovascular
* 0 indica que o paciente não tem doença cardiovascular

## Variáveis do dataset
O dataset contém as seguintes variáveis:
* `age`  idade dos pacientes
* `gender`  gênero (2 mulheres, 1 homens)
* `height`  altura
* `weight`  peso
* `gluc`  glicose
* `smoke`  fumante (1) ou não fumante (0)
* `alco`  consome álcool (1) ou não consome (0)
* `active`  realiza atividade física (1) ou não realiza (0)
* `cardio_disease`  variável alvo

## Principais etapas do projeto
1. Carregamento e validação inicial da base
   * leitura do arquivo CSV
   * checagem de tipos de dados, valores faltantes e outliers

2. Exploração dos dados e criação de variáveis auxiliares
   * criação de labels para padronização e análise
   * visualizações para investigar distribuição e incidência por categoria
   * análise de idade e IMC em relação à variável alvo

3. Correlação
   * construção de matriz de correlação para avaliar relacionamentos lineares
   * destaque para correlações fracas no geral e maior associação do alvo com idade

4. Pré modelo
   * remoção de colunas não usadas no treino
   * separação treino e teste
   * padronização das variáveis contínuas `age` e `imc` com StandardScaler

5. Modelagem
   * treinamento de Regressão Logística
   * avaliação com relatório de classificação e curva ROC

## Resultados
Avaliação no conjunto de teste:
* Accuracy: 0.65
* AUC: 0.65

Relatório de classificação:
* Classe 0
  * precision: 0.64
  * recall: 0.69
  * f1 score: 0.66
* Classe 1
  * precision: 0.66
  * recall: 0.61
  * f1 score: 0.64

## Como executar o projeto
### Requisitos
* Python 3
* Bibliotecas: pandas, numpy, matplotlib, plotly, seaborn, scikit learn, imbalanced learn

### Passo a passo
1. Clone o repositório
2. Coloque o arquivo `CARDIO_BASE.csv` na mesma pasta do notebook, ou ajuste o caminho no `read_csv`
3. Abra e rode o notebook:
   * `notebooks/Profissao_Cientista_de_Dados_M27_Pratique.ipynb`

O dataset é lido assim:
* arquivo: `CARDIO_BASE.csv`
* separador: `;`

## Estrutura sugerida do repositório
* `README.md`
* `notebooks/Profissao_Cientista_de_Dados_M27_Pratique.ipynb`
* `data/CARDIO_BASE.csv`

## Próximos passos
* testar outros modelos de classificação e comparar métricas
* explorar ajuste de limiar de decisão
* aplicar validação cruzada e tuning de hiperparâmetros
* incluir interpretabilidade do modelo para entender impacto das variáveis
