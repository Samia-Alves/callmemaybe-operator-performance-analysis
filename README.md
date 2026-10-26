# CallMeMaybe | Análise do desempenho de operadores

**Projeto de portefólio em Análise de Dados · TripleTen · 2026**

Análise exploratória e estatística de dados de um serviço de telefonia virtual para identificar **sinais de possíveis dificuldades operacionais** e apoiar a tomada de decisão. O projeto inclui um notebook em Python, uma apresentação executiva e um dashboard em Tableau.

### 📊 [Explorar o dashboard interativo no Tableau](https://public.tableau.com/app/profile/samia.alves/viz/CallMeMaybeAnliseOperacionaldeOperadores/Painel1)

## Problema de negócio

A CallMeMaybe pretende compreender o desempenho dos operadores de atendimento e identificar situações que justifiquem acompanhamento. A análise considera três indicadores:

- Proporção de chamadas recebidas perdidas;
- Tempo médio de espera nas chamadas recebidas;
- Volume de chamadas de saída por dia com atividade registada.

Os indicadores são avaliados com critérios mínimos de atividade, para evitar comparações pouco representativas.

## Ferramentas e competências

**Python · pandas · NumPy · Matplotlib · Seaborn · SciPy · Jupyter Notebook · Tableau**

Preparação e limpeza de dados, análise exploratória, construção de indicadores operacionais, testes estatísticos (correlação de Spearman), visualização e comunicação de resultados.

## Metodologia

1. **Preparação dos dados:** análise de duplicados, valores em falta, tipos de dados e consistência dos registos.
2. **Análise exploratória:** evolução temporal das chamadas, diferenças entre chamadas de entrada e saída e distribuição das chamadas perdidas.
3. **Indicadores por operador:** cálculo de métricas e aplicação de critérios mínimos de participação.
4. **Consolidação de alertas:** identificação de operadores com um ou mais sinais que merecem investigação.
5. **Testes estatísticos:** estudo exploratório de associações entre indicadores com correlação de Spearman.
6. **Comunicação:** apresentação de conclusões e dashboard interativo.

## Principais resultados

| Indicador | Resultado |
|---|---:|
| Operadores identificados | 1.092 |
| Operadores elegíveis para pelo menos uma avaliação | 564 |
| Operadores com pelo menos um alerta | 214 (37,94%) |
| Operadores com dois ou três alertas | 44 |
| Operadores com três alertas | 9 |

**Resultados estatísticos:**

- Taxa de chamadas perdidas e tempo médio de espera: **ρ = 0,1460**, **p = 0,011928** — associação positiva muito fraca.
- Tempo médio de espera e volume de chamadas de saída por dia ativo: **ρ = −0,3171**, **p = 0,000003** — associação negativa fraca a moderada.

As associações observadas **não demonstram causalidade** nem permitem concluir, isoladamente, que um operador é ineficiente.

## Limitações e recomendações

Uma parte muito significativa das chamadas perdidas de entrada não possui operador identificado. Por isso, **a taxa geral de chamadas perdidas não deve ser atribuída diretamente a operadores individuais**. Também faltam informações sobre jornadas, funções, distribuição de tarefas e metas operacionais.

A análise recomenda:

- Investigar prioritariamente os **44 operadores com múltiplos alertas**, considerando o contexto de trabalho;
- Melhorar o registo da identificação dos operadores nas chamadas perdidas;
- Acompanhar os tempos de espera e os volumes de chamadas com indicadores contextualizados;
- Utilizar os alertas como ponto de partida para investigação, e não como avaliação definitiva de desempenho.

## Ficheiros do projeto

- [`Projeto_Final_CallMeMaybe.ipynb`](Projeto_Final_CallMeMaybe.ipynb) — análise completa em Python;
- [`CallMeMaybe_Apresentacao_Samia_Alves.pdf`](CallMeMaybe_Apresentacao_Samia_Alves.pdf) — apresentação dos resultados;
- [`dashboard.txt`](dashboard.txt) — ligação para o dashboard no Tableau.

> **Nota sobre os dados:** o notebook utiliza os ficheiros `telecom_dataset_us.csv` e `telecom_clients_us.csv`, originalmente lidos a partir de `/datasets/`. Estes ficheiros não estão incluídos neste repositório. Para executar o notebook noutro ambiente, é necessário obter os dados através da fonte autorizada e ajustar os caminhos de leitura.

---

**Autora:** Samia Alves · [LinkedIn](https://www.linkedin.com/in/samia-alves-a8baa51b0) · [GitHub](https://github.com/Samia-Alves)
