# Análise de Filmes IMDB 

## Contexto  
Este projeto foi desenvolvido como parte de um **desafio para uma vaga de trainee** em análise de dados  

A base fornecida contém informações de **999 filmes do IMDb**, incluindo variáveis como título, ano de lançamento, gênero, número de votos, bilheteria, avaliação do público, entre outras  

O objetivo é **explorar os dados, gerar insights e responder perguntas-chave** relacionadas ao comportamento dos filmes e seus atributos

---

##  Objetivos do Desafio  

1. **Análise Exploratória dos Dados (EDA):**  
   - Explorar as principais características das variáveis
   - Levantar hipóteses e possíveis correlações  
   - Identificar padrões e outliers  

2. **Questões a Responder:**  
   - Qual filme você recomendaria para uma pessoa que você não conhece?  
   - Quais são os principais fatores relacionados à **alta expectativa de faturamento** de um filme?  
   - Quais insights podem ser tirados a partir da coluna **Overview**?  
     - É possível inferir o gênero do filme a partir dessa descrição?  
   - Como prever a **nota do IMDb** de um filme com base nas variáveis disponíveis?  
     - Quais variáveis/transformações foram usadas?  
     - Que tipo de problema estamos resolvendo (regressão ou classificação)?  
     - Qual modelo melhor se aproxima dos dados? Quais prós e contras?  
     - Qual métrica de avaliação foi escolhida e por quê?  

3. **Caso de Teste:**  
   - Supondo um filme com as seguintes características:  

```python
{
 'Series_Title': 'The Shawshank Redemption',
 'Released_Year': '1994',
 'Certificate': 'A',
 'Runtime': '142 min',
 'Genre': 'Drama',
 'Overview': 'Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.',
 'Meta_score': 80.0,
 'Director': 'Frank Darabont',
 'Star1': 'Tim Robbins',
 'Star2': 'Morgan Freeman',
 'Star3': 'Bob Gunton',
 'Star4': 'William Sadler',
 'No_of_Votes': 2343110,
 'Gross': '28,341,469'
}
```
4. **Metodologia**
- **Linguagem:** Python  

- **Principais pacotes utilizados:**  
  - `pandas`, `numpy` → manipulação de dados  
  - `matplotlib`, `seaborn` → visualizações  
  - `scikit-learn` → modelagem e métricas  
  - `statsmodels`, `scipy` → testes estatísticos  
  - `featuretools` → engenharia de atributos  
  - `requests` → coleta complementar de dados  

- **Fluxo do projeto:**  
  1. Limpeza e tratamento da base
  2. EDA com tabelas e gráficos
  3. Missing imputation e Feature Engineering
  4. Construção de modelos preditivos (classificação) com Random Forest e Gradient Boosting  
  5. Avaliação e interpretação dos resultados
  6. Tentativa de extração de gênero por Overview
5. **Principais Resultados**
- Extração de variáveis adicionais usando a API do TMDB
- Lançamentos são mais lucrativos em meses de férias
- Semana de lançamento possui pouca influência no ROI
- A nota do filme não influencia significativamente no ROI, mas o número de votos sim
- Ausência de evidências de que um investimento maior no filme melhor sua nota
- Investimento em marketing pode ser uma boa estratégia para aumentar o ROI em filmes de baixo orçamento
- Criação de um modelo GB com R² = 0.789 e MSE = 0.01
- Dificuldades em criar um modelo de classificação para os gêneros com base em overview pela má distribuição dos dados
