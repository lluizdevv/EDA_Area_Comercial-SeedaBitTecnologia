# 📊 EDA Comercial — Seed a Bit (2022–2026)

> Análise Exploratória de Dados da Área Comercial da Seed a Bit Tecnologia, cobrindo o histórico completo de contratos fechados entre 2022 e 2026.

---

## 📋 Sobre o Projeto

Este notebook foi desenvolvido no contexto do **Processo Eleitoral (PROEL)** da Seed a Bit Tecnologia com o objetivo de organizar, visualizar e extrair insights estratégicos sobre o histórico comercial da área de Negócios. A partir de dados reais de contratos fechados entre 2022 e 2026, o notebook oferece uma visão analítica completa que serve como base para decisões de gestão, elaboração de propostas e diagnóstico da evolução comercial da empresa.

O projeto segue a metodologia **KDD (Knowledge Discovery in Databases)**, partindo da preparação dos dados, passando pela análise exploratória univariada e multivariada, até a geração de insights comerciais acionáveis.

---

## 🎯 Objetivos

- Consolidar e organizar os dados históricos de contratos da área comercial em um único lugar
- Analisar a evolução do faturamento, ticket médio e mix de serviços ao longo dos anos
- Identificar padrões de origem dos contratos e sua transformação ao longo do tempo
- Mapear sazonalidade, constância de fechamentos e concentração de risco por contrato
- Analisar a fidelização e taxa de retenção de clientes
- Gerar insights estratégicos que subsidiem decisões da diretoria e gerência comercial

---

## 🗂️ Estrutura do Notebook

| Seção | Descrição |
|---|---|
| **0. Setup e Preparação** | Importação de bibliotecas, configuração do estilo visual e definição dos dados brutos por ano (2022–2026) |
| **1. Análise Univariada** | Distribuição de faturamento, ticket médio por ano e serviço, frequência de serviços e sazonalidade |
| **2. Análise Bivariada e Multivariada** | Cruzamentos entre origem, serviço, ano, ritmo acumulado, projetos colaborativos e fidelização |
| **3. Insights Comerciais** | Síntese analítica com conclusões estratégicas para tomada de decisão |

---

## 📊 Análises Incluídas

### Análise Univariada
- `u1` — Distribuição dos valores de contrato (histograma + boxplot por ano)
- `u2` — Faturamento total anual vs Meta
- `u3` — Evolução do ticket médio geral por ano
- `u4` — Ticket médio por tipo de serviço (histórico)
- `u5` — Frequência de tipos de serviço vendidos (2022–2026)
- `u6` — Sazonalidade — faturamento acumulado por mês
- `u7` — Meses sem fechamento de contrato por ano
- `u8` — Mix de serviços por ano (participação % no faturamento)
- `u9` — Mix de origens por ano (participação % no faturamento)
- `u10` — Quantidade de contratos por tipo de serviço por ano

### Análise Bivariada e Multivariada
- `b1` — Curvas de faturamento acumulado vs ritmo significativo por ano
- `b2` — Composição do faturamento anual por tipo de serviço (barras empilhadas)
- `b3` — Distribuição de valores por tipo de serviço (boxplot)
- `b4` — Ticket médio e distribuição por origem do contrato
- `b5` — Heatmap Origem × Tipo de Serviço (faturamento total)
- `b6` — Projetos colaborativos vs não-colaborativos por ano
- `b7` — Dispersão mês de fechamento × valor do contrato
- `b8` — Composição do faturamento anual por origem
- `b9` — Evolução do ticket médio por tipo de serviço ao longo dos anos
- `b10` — Número de contratos vs faturamento total por ano (eixo duplo)
- `b11` — Taxa de fidelização: novos leads vs clientes recorrentes por ano

---

## 💡 Principais Insights

**Crescimento e maturidade comercial:** A Seed a Bit acumulou mais de R$ 264.000 em faturamento entre 2022 e 2026 (parcial), com crescimento de aproximadamente 329% em 4 anos. O padrão de crescimento evoluiu de alta dependência de poucos contratos grandes para uma carteira progressivamente mais diversificada.

**Efeito dos contratos-âncora:** Em todos os anos, 1 ou 2 contratos foram responsáveis por mais de 30% do faturamento total (Alpha Tech em 2022, Fenix Research em 2024, Heath Plus em 2025, Prime Development em 2026). Esse padrão representa tanto uma capacidade de fechar contratos de alto valor quanto um risco estrutural de concentração de receita.

**Declínio da dependência institucional:** Em 2022, 100% dos contratos vieram de origem institucional. Em 2025, prospecção ativa tornou-se a principal origem, com indicação, recorrência e marketing também presentes — indicando maturidade comercial real.

**Recorrência como canal estratégico subutilizado:** A recorrência aparece como origem relevante a partir de 2023 e cresce de forma consistente até 2026, com custo de aquisição zero e tendência de ticket crescente. Em 2026, já responde por mais de 60% do faturamento — mas ainda opera de forma orgânica, sem gestão deliberada.

**Sazonalidade e constância:** Os meses de maio, julho e agosto historicamente concentram os maiores volumes de faturamento. A constância de fechamentos — medida por meses sem contrato — melhorou significativamente entre 2022 (meses vazios em excesso) e 2025 (apenas 1 mês sem fechamento).

**Fidelização em evolução:** 2026 apresenta o melhor mix histórico de fidelização, com 33,3% de aditivos no mesmo ano e 8,3% de retorno de clientes de anos anteriores, indicando que a área está amadurecendo na gestão de relacionamento com clientes já existentes.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas** — manipulação e estruturação dos dados
- **NumPy** — operações numéricas
- **Matplotlib** — visualizações customizadas com tema dark
- **Seaborn** — heatmaps e boxplots complementares
- **Jupyter Notebook / Google Colab** — ambiente de execução

---

## ⚙️ Como Executar

### No Google Colab (recomendado)

1. Faça o upload do notebook no Google Colab
2. Ajuste o caminho de carregamento dos dados caso necessário (indicado com comentário `⚠️` no notebook)
3. Execute todas as células em sequência (`Runtime > Run all`)
4. Os gráficos gerados serão salvos automaticamente em `/content/` com os prefixos `u` (univariada) e `b` (bivariada)

### Localmente

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook EDA_Área_Comercial_Seed_a_Bit__2022_2026_.ipynb
```

---

## 📁 Arquivos Gerados

Ao executar o notebook completo, os seguintes arquivos de imagem são gerados automaticamente:

```
u1_distribuicao_faturamento.png
u2_faturamento_vs_meta.png
u3_ticket_medio_por_ano.png
u4_ticket_medio_por_servico.png
u5_frequencia_servicos.png
u6_sazonalidade.png
u7_meses_sem_contrato.png
u8_pizza_servicos_por_ano.png
u9_pizza_origens_por_ano.png
u10_pizza_qtd_contratos_por_ano.png
b1_curvas_acumuladas.png
b2_composicao_servicos.png
b3_boxplot_servico.png
b4_origem_faturamento.png
b5_heatmap_origem_servico.png
b6_colaborativo.png
b7_dispersao_mes_valor.png
b8_composicao_origens.png
b9_ticket_servico_evolucao.png
b10_contratos_vs_faturamento.png
```

---

## 📌 Observações

- Os dados de 2026 cobrem apenas o primeiro semestre (janeiro a junho), sendo portanto parciais em relação aos anos anteriores
- O campo `colaborativo` identifica contratos realizados em parceria com outras empresas juniores ou organizações externas
- As origens dos contratos são classificadas em cinco categorias: `institucional`, `indicação`, `prospecção_ativa`, `recorrência` e `marketing`
- O notebook foi desenvolvido com tema visual dark (fundo `#0D1B2E`) para facilitar a leitura dos gráficos em apresentações

---

## 👥 Autor

Luiz Vinicius - Analista de Negócios e candidato à Diretoria de Negócios na **Seed a Bit Tecnologia**.

**Seed a Bit Tecnologia** — Empresa Júnior da Universidade Federal Rural de Pernambuco (UFRPE), federada à FEJEPE.

> *"Em cada pequena semente, enxergamos uma farta colheita."*
