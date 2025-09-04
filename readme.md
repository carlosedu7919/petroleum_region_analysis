# Projeto de Previsão de Lucro em Exploração de Petróleo

Este projeto tem como objetivo identificar a região mais vantajosa para investimento em exploração de petróleo, utilizando modelagem preditiva, análise de risco e critérios financeiros definidos pelo desafio.

---

## Sumário

- [Descrição do Projeto](#descrição-do-projeto)
- [Fluxo do Projeto](#fluxo-do-projeto)
- [Como Executar](#como-executar)
- [Principais Resultados](#principais-resultados)
- [Conclusão e Recomendação](#conclusão-e-recomendação)
- [Estrutura dos Arquivos](#estrutura-dos-arquivos)
- [Requisitos](#requisitos)

---

## Descrição do Projeto

O projeto consiste em analisar dados de três regiões de exploração, treinar modelos preditivos para estimar o volume de reservas em cada poço, selecionar os 200 poços mais promissores por região e calcular o lucro potencial esperado. Por fim, é aplicada a técnica de bootstrapping para avaliar o risco de prejuízo e definir a região mais segura e lucrativa para investimento.

---

## Fluxo do Projeto

1. **Preparação dos Dados**
   - Limpeza, análise exploratória e separação das regiões.
2. **Modelagem Preditiva**
   - Treinamento de modelos de regressão para prever o volume de reservas.
   - Avaliação dos modelos com métricas como RMSE e volume médio previsto.
3. **Seleção dos 200 Melhores Poços**
   - Seleção dos poços com maior previsão de produção em cada região.
4. **Cálculo do Lucro Potencial**
   - Receita: volume total previsto × \$4.500 por mil barris.
   - Custo: \$100 milhões para 200 poços.
   - Lucro: receita – custo.
5. **Análise de Risco (Bootstrapping)**
   - Simulação de cenários para estimar o risco de prejuízo e o intervalo de confiança do lucro.
6. **Conclusão**
   - Recomendação da região mais segura e lucrativa de acordo com os critérios do projeto.

---

## Como Executar

1. **Clone o repositório:**

2. **Instale as dependências:**

pip install -r requirements.txt

3. **Execute o notebook principal:**
- Abra e siga o passo a passo no arquivo `.ipynb` (Jupyter Notebook).

---

## Principais Resultados

| Região    | Lucro Médio ($)    | Intervalo de Confiança 95% ($)          | Probabilidade de Prejuízo (%) |
|-----------|--------------------|------------------------------------------|-------------------------------|
| Região 0  | 4.331.084,40       | -652.942,65 a 9.724.072,82               | 3,60                          |
| Região 1  | 4.365.546,01       | 417.167,78 a 8.215.891,71                | 1,80                          |
| Região 2  | 3.692.290,85       | -1.360.008,05 a 8.492.361,99             | 8,20                          |

---

## Conclusão e Recomendação

- **Apenas a Região 1 é elegível para investimento**, pois apresenta risco de prejuízo inferior ao limite de 2,5% estabelecido pelo projeto e também o maior lucro médio entre as regiões que atendem ao critério.
- As demais regiões devem ser descartadas devido ao risco de perdas acima do permitido.

Esses resultados orientam a decisão estratégica, priorizando segurança financeira e retorno esperado conforme as regras do projeto.

---

## Estrutura dos Arquivos

- `notebook.ipynb` — Notebook principal com todo o fluxo do projeto.
- `requirements.txt` — Lista de dependências Python.
- `README.md` — Este arquivo de apresentação do projeto.
- `data/` — Pasta com os dados das três regiões.

---

## Requisitos

- Python 3.7+
- Pandas, NumPy, scikit-learn, Jupyter Notebook

---

Se tiver dúvidas, sugestões ou quiser contribuir, fique à vontade para abrir uma issue ou pull request!


