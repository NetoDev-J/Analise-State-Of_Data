# José Alves e Enzo Santos — State of Data Brazil 2024–2025

**Disciplina:** Análise Avançada de Dados — UNIFSA    
**Dashboard:** [Acesse aqui]([LINK_DO_DASHBOARD])

---

## Pergunta central

**Quais fatores mais influenciam o salário de um profissional de dados no Brasil em 2024?**

Com base na análise do State of Data Brazil 2024–2025, identificamos que os fatores
com maior influência sobre o salário são o nível de senioridade e o tempo de experiência
em dados. A progressão de Júnior para Sênior representa uma multiplicação de 4x na
mediana salarial (de R$3.500 para R$14.000), enquanto a correlação de Spearman entre
senioridade e salário foi de 0,734, a mais alta entre todas as variáveis analisadas.

O tempo de experiência também se mostrou relevante (Spearman: 0,633), com o principal
salto salarial ocorrendo entre as faixas de 1–2 anos e 3–4 anos, onde a mediana dobra
de R$5.000 para R$10.000. A partir dos 5 anos, o salário estabiliza em R$14.000,
sugerindo que a experiência isolada deixa de ser diferencial após certo ponto.

Em relação ao gênero, não há diferença salarial entre Júniores e Plenos, mas no nível
Sênior mulheres recebem mediana de R$10.000 contra R$14.000 dos homens, uma diferença
de 40% que persiste mesmo controlando pelo nível de carreira.

---

## Principais decisões de limpeza

- **Faixas salariais:** convertidas para ponto médio numérico (ex: "de R$4.001 a R$6.000" → R$5.000). A faixa superior foi atribuída como R$45.000. Essa decisão introduz imprecisão reconhecida na análise.
- **Gênero e raça/cor:** missings não foram imputados pois representam escolha do respondente de não informar. Mantidos como categoria "Não informado".
- **Cargos:** padronizados via mapeamento explícito agrupando variações em português e inglês.
- **Colunas binárias de linguagem:** 229 registros com ausência total nas colunas de linguagem foram imputados com 0, pois todos pertenciam aos mesmos respondentes que pularam a questão integralmente.
- **Renomeação:** 12 colunas-chave renomeadas com base no dicionário oficial antes de qualquer análise.

---

## Estrutura do repositório

```
JoseAlves-EnzoSantos-state-of-data/
├── README.md
├── notebook/
│   └── JoseAlves-EnzoSantos-analise.ipynb
├── relatorio/
│   └── JoseAlves-EnzoSantos-relatorio.pdf
└── dados/
    └── README.md
```

---

## Referências

- Base de dados: [State of Data Brazil 2024–2025](https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025) — Data Hackers & Bain & Company
- Bibliotecas: pandas, numpy, matplotlib, seaborn, scipy
