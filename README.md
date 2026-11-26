# Estatística geral com Python

Notebooks Jupyter de estudo de estatística geral: em cada tema, primeiro a teoria (em Markdown, com fórmulas em LaTeX), depois exemplos e exercícios resolvidos em Python. Os cálculos usam NumPy e SciPy, e os gráficos e diagramas são gerados com Matplotlib. Os testes de hipóteses dos notebooks 4 e 5 foram escritos à mão (tabelas Z e t-Student, região crítica, valor-p e intervalo de confiança); no notebook 6, o teste F usa os valores críticos de `scipy.stats.f`, e os testes t para duas médias usam as funções prontas `scipy.stats.ttest_ind_from_stats` e `scipy.stats.ttest_rel`.

Todo o conteúdo está em português.

## Conteúdo

| Notebook | Temas |
|---|---|
| `1 - Estatística básica.ipynb` | Distribuição de frequência, medidas de tendência central, medidas de dispersão, escore Z, quantis, quartis, intervalo interquartil e outliers |
| `2 - Probabilidade.ipynb` | Axiomas, probabilidade condicional, teorema de Bayes, variáveis aleatórias discretas e contínuas, distribuições binomial, Poisson, exponencial e normal, com exercícios |
| `3 - Estimação de parâmetros estatísticos.ipynb` | Estimativa pontual e intervalar, intervalos de confiança para a média (σ conhecido e desconhecido) e para a proporção, tamanho da amostra |
| `4 - Testes de hipóteses.ipynb` | Hipóteses nula e alternativa, tipos de erro, região crítica, valor-p, teste z e teste t para uma média, teste para uma proporção |
| `5 - Teste Z para duas proporções.ipynb` | Comparação de duas proporções com teste Z |
| `6 - Teste T para duas médias.ipynb` | Teste F para duas variâncias; teste t para duas médias independentes (variâncias iguais e desiguais) e para amostras pareadas |

## Como executar

Requisitos: Python 3, NumPy, SciPy, Matplotlib e Jupyter. Os notebooks não leem arquivos externos; os dados de cada exercício estão no próprio código.

```bash
git clone https://github.com/guilherme-b-azevedo/Estatistica-geral-com-python.git
cd Estatistica-geral-com-python
python -m venv .venv
# Windows: .venv\Scripts\activate    Linux/macOS: source .venv/bin/activate
pip install numpy scipy matplotlib notebook
jupyter notebook
```

Execute as células de cada notebook em ordem, de cima para baixo: as funções auxiliares (busca nas tabelas Z e t, tipo de região crítica, desenho dos gráficos) são definidas em células anteriores aos exemplos. Para resolver um problema seu, altere as variáveis do enunciado na célula do exemplo e execute de novo.

Versões: os notebooks foram salvos em 2020 com Python 3.7.1. Em novembro de 2026, o código das células rodou com Python 3.14, NumPy 2.4 e SciPy 1.17 (executado fora do Jupyter), e as células de gráficos e de consulta às tabelas acrescentadas nessa revisão foram executadas num kernel Jupyter com Python 3.12, NumPy 2.5, SciPy 1.18 e Matplotlib 3.11.

## Exemplo

`5 - Teste Z para duas proporções.ipynb` compara duas amostras (A: 144 sucessos em 160; B: 130 em 150), com significância de 10% e hipótese alternativa unilateral à direita. Saída do notebook (trecho):

```
H0:  0.9_<=_0.8667
Ha:  0.9_>_0.8667

Alfa:  0.1
Valor crítico:  1.28
Estimativa ponderada:  0.8839

Estatística de teste:  0.9146
P valor:  0.180201

H0 aceitada, pois P-valor 0.180201 >= Alfa 0.1
```

## Situação

Projeto de estudo e portfólio, de 2020. Não está em desenvolvimento ativo.

## Licença

Distribuído sob a licença MIT. Veja o arquivo [LICENSE](LICENSE).
