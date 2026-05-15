# 📈 Análise de Ações Brasileiras — B3 (Jan/2023 a Mai/2026)

Projeto acadêmico de análise financeira de quatro empresas listadas na B3, desenvolvido em Python no Google Colab. O script baixa dados históricos via `yfinance` e realiza análise descritiva completa com estatísticas semestrais e visualizações.

---

## 🏢 Empresas Analisadas

| Empresa            | Ticker (Yahoo Finance) |
|--------------------|------------------------|
| Petrobrás          | PETR4.SA               |
| Banco do Brasil    | BBAS3.SA               |
| Ambev S.A.         | ABEV3.SA               |
| Itaú Unibanco      | ITUB4.SA               |
| Vale S.A.          | VALE3.SA               |

**Período:** janeiro de 2023 a maio de 2026

---

## 🔍 O que o script faz

Para cada empresa, o código executa as seguintes etapas:

1. **Download dos dados históricos** via `yfinance` (Abertura, Máxima, Mínima, Fechamento, Volume)
2. **Visualização das primeiras e últimas linhas** do DataFrame
3. **Média anual** do preço de fechamento (2023–2026)
4. **Desvio-padrão anual** do preço de fechamento
5. **Retorno semestral** — variação percentual entre semestres consecutivos (ex: 2023-S1 → 2023-S2)
6. **Gráfico de linha** do preço de fechamento com eixo X rotulado por semestre e marcação dos fins de período
7. **Tabela resumo semestral** com abertura, fechamento, média, desvio-padrão, mínimo, máximo e retorno
8. **Resumo final do período** com retorno total acumulado e volume médio diário

---

## 🛠️ Tecnologias e Bibliotecas

- Python 3
- [yfinance](https://pypi.org/project/yfinance/) — coleta de dados históricos de ações
- [pandas](https://pandas.pydata.org/) — manipulação e análise de dados
- [matplotlib](https://matplotlib.org/) — geração de gráficos
- [seaborn](https://seaborn.pydata.org/) — estilização dos gráficos

---

## ▶️ Como executar

O projeto foi desenvolvido para rodar diretamente no **Google Colab**. Basta abrir o notebook e executar as células em sequência — as dependências são instaladas automaticamente via `!pip install`.

Para rodar localmente, instale as dependências:

```bash
pip install yfinance pandas matplotlib seaborn
```

Em seguida, execute o script:

```bash
python adminanáliseações.py
```

> **Nota:** o arquivo foi exportado de um notebook Colab. Comandos com `!` (como `!pip install`) são específicos do ambiente Colab/Jupyter e podem precisar de ajuste para execução local.

---

## 📁 Estrutura do Projeto

```
.
├── adminanáliseações.py   # Script principal com análise de todas as empresas
└── README.md
```

---

## 📊 Exemplo de Saída

```
📥 Baixando dados da PETR4.SA de 2023-01-01 até 2026-05-14...
✅ Dados carregados! Shape: (831, 5)

📊 MÉDIA ANUAL DO PREÇO DE FECHAMENTO (R$)
2023: R$ 35.42
2024: R$ 38.17
...

📊 RETORNO SEMESTRAL DO PREÇO DE FECHAMENTO (%)
2023_S1 → 2023_S2: -4.83%
2023_S2 → 2024_S1: +12.41%
...
```

---

## 👩‍💻 Autora

Desenvolvido como exercício acadêmico para a disciplina de Administração — análise de dados financeiros com Python.
