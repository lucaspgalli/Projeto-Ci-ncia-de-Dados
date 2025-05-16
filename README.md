# Análise de Gastos Públicos por Área — Projeto de Ciência de Dados

## Pergunta Orientadora
**Como é distribuído os gastos públicos entre áreas como saúde, educação e segurança ao longo do ano?**

---

## Objetivo
Este projeto tem como objetivo analisar a **distribuição de gastos públicos** entre diferentes áreas temáticas (como saúde, educação e segurança), com base em dados abertos. A análise visa identificar **padrões de alocação orçamentária**, **tendências ao longo do tempo** e **diferenças entre áreas** ao longo do ano.

---

## Fonte de Dados
Os dados utilizados foram obtidos a partir do portal [Gov.br - Execução da Despesa](https://portaldatransparencia.gov.br/download-de-dados/despesas-execucao) em formato `.csv`, contendo informações detalhadas sobre despesas públicas.

---

## Etapas Realizadas

### 1. Detecção de Codificação
Foi utilizada a biblioteca `chardet` no Google Colab para detectar automaticamente a codificação correta dos arquivos `.csv`, evitando erros na leitura de dados com acentos e caracteres especiais.

### 2. Leitura e Consolidação dos Arquivos
Todos os arquivos foram carregados e armazenados em uma lista de `DataFrames` com `pandas`. Os dados foram então consolidados em um único arquivo `execucao_despesa_consolidado.csv`.

### 3. ETL no Power BI
O arquivo consolidado foi importado no Power BI, onde foi realizado:
- Tratamento de dados.
- Criação de novas colunas para facilitar a análise.
- Modelagem dos dados para visualizações.

### 4. Criação de Medidas e Gráficos
Foram criadas medidas no Power BI, incluindo:
- **Total Valor Pago**
- **Total Valor Liquidado**
- **Diferença** (entre pago e liquidado)

Com isso, foram construídos dashboards com:
- **Top 10 Funções com Maior Valor Pago**
- **Top 10 Órgãos Superiores com Maior Valor Pago**

Ambos os gráficos foram filtrados dinamicamente com base na soma do valor pago, utilizando filtros de hierarquia para destacar as entidades mais relevantes.

---

## Ferramentas Utilizadas

### Python (Google Colab)
- `pandas`
- `glob`

### Power BI
- Transformações de dados (ETL)
- Criação de medidas DAX
- Visualizações interativas

