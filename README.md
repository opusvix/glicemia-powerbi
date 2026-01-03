# 📊 Monitoramento e Análise de Glicemia com Power BI

## 📌 Visão Geral
Este projeto tem como objetivo analisar dados de glicemia coletados diariamente, explorando padrões temporais, comportamento por refeição, impacto da rotina e variações entre dias úteis e fins de semana.

O dashboard foi desenvolvido no **Power BI**, utilizando boas práticas de **modelagem de dados**, **DAX**, **tabela calendário** e **storytelling com dados**, com foco em gerar insights claros e acionáveis.

---

## 🎯 Objetivo do Projeto
- Monitorar a evolução da glicemia ao longo do tempo  
- Identificar padrões por refeição (jejum, almoço e jantar)  
- Avaliar o impacto da rotina alimentar e horários  
- Comparar comportamento glicêmico entre dias úteis e fins de semana  
- Transformar dados de saúde em informação visual para apoio à tomada de decisão  

---

## 🗂️ Fonte dos Dados
- Dados reais de medições de glicemia
- Coleta diária
- Estrutura em Excel
- Período contínuo de acompanhamento

> ⚠️ Os dados não contêm informações sensíveis ou identificáveis.

---

## 🧱 Modelagem de Dados

### 📅 Tabela Calendário
Foi criada uma tabela calendário dedicada para:
- Análises temporais
- Segmentação por dia da semana
- Identificação de fins de semana
- Análises mensais e acumuladas

Relacionamento:
- dCalendario[Date] 1 ──── * fGlicemia[Data]

---

## 📐 Principais Medidas DAX

- Média de glicemia em jejum
- Média por refeição
- Média geral diária
- Média móvel (7 dias)
- Classificação por faixa glicêmica
- Comparação entre dias úteis e fins de semana
- Análise de horários (dispersão)

Exemplo:
```DAX
Media Geral Glicemia =
AVERAGEX (
    fGlicemia,
    DIVIDE (
        fGlicemia[GlicemiaJejum]
        + fGlicemia[GlicemiaAlmoco]
        + fGlicemia[GlicemiaJantar],
        3
    )
)
````
## 📊 Estrutura do Dashboard

🔹 Página 1 — Visão Geral

  - KPIs principais
  - Evolução da glicemia em jejum
  - Média móvel
  - Segmentadores de data

🔹 Página 2 — Análise por Refeição

  - Comparação entre jejum, almoço e jantar
  - Distribuição dos valores
  - Identificação de picos

🔹 Página 3 — Rotina e Comportamento

  - Dias úteis × fins de semana
  - Análise por dia da semana
  - Dispersão: horário × glicemia

🔹 Página 4 — Detalhamento Diário

  - Tabela detalhada
  - Formatação condicional
  - Observações por data

## 💡 Principais Insights

  - Fins de semana apresentam média glicêmica superior aos dias úteis
  - Horários mais tardios de refeição tendem a se associar a níveis mais elevados de glicemia
  - O controle glicêmico é mais estável em dias de rotina regular
  - A glicemia antes do jantar apresenta maior variabilidade

## 🧠 Tecnologias Utilizadas

  - Power BI

  - DAX

  - Excel

  - Modelagem Dimensional

  - Storytelling com Dados

## 🚀 Próximos Passos

  - Inclusão de metas parametrizadas
  
  - Expansão da série histórica
  
  - Comparação mensal e trimestral
  
  - Análises preditivas futuras

## 👤 Autor    
  Maurício Barros    
  Analista de Dados    
  🔗 GitHub: https://github.com/opusvix

  

