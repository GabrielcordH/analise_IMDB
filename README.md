# Análise de Filmes IMDb  

## 📌 Contexto  
Este projeto foi desenvolvido como parte de um **desafio para uma vaga de trainee** em análise de dados.  

A base fornecida contém informações de **999 filmes do IMDb**, incluindo variáveis como título, ano de lançamento, gênero, número de votos, bilheteria, avaliação do público, entre outras.  

O objetivo é **explorar os dados, gerar insights e responder perguntas-chave** relacionadas ao comportamento dos filmes e seus atributos.  

---

## 📝 Objetivos do Desafio  

1. **Análise Exploratória dos Dados (EDA):**  
   - Explorar as principais características das variáveis.  
   - Levantar hipóteses e possíveis correlações.  
   - Identificar padrões e outliers.  

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
