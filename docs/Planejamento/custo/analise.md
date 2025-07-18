# Planejamento de custo - Análise

## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 17/05/2025 | Adiciona análise do planejamento de custo     | Jackes        |

---

Este documento tem como objetivo analisar os gráficos de custo e entender seu comportamento.

## Valor Planejado(PV) X Custo Real(AC)
Essa comparação permite entender se o projeto está dentro do orçamento em relação ao que estava previsto para o momento atual. O Valor Planejado (PV) representa quanto deveria ter sido gasto com base no planejamento, enquanto o Custo Real (AC) indica quanto foi efetivamente gasto até o momento.
- Se AC > PV, o projeto está gastando mais do que o previsto para essa etapa.
- Se AC < PV, o projeto gastou menos do que o esperado.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-0.png)

## Porcentagem Planejada Concluída(PPC) X Porcentagem Real Concluída(PRC)
Compara o progresso teórico com o progresso real.
- A Porcentagem Planejada Concluída (PPC) é quanto do trabalho deveria estar finalizado de acordo com o cronograma.
- A Porcentagem Real Concluída mostra quanto de fato foi realizado.

Essa comparação evidencia atrasos ou adiantamentos no desenvolvimento.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-1.png)

## Valor Planejado(PV) X Valor Agregado(EV)
Essa análise mede o progresso do projeto em termos de valor.
- PV mostra o valor que deveria ter sido criado até o momento.
- EV mostra o valor que foi efetivamente criado.
    - Se EV < PV, o projeto está atrasado.
    - Se EV > PV, está adiantado.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-2.png)

## Variação do Custo(CPV) X Variação do Prazo(SPV)
Aqui, são analisadas duas variações essenciais:
- CVP = EV - AC → mostra se houve economia ou estouro de orçamento.
- SVP = EV - PV → mostra se houve atraso ou adiantamento no cronograma.

Essas variáveis ajudam a entender se o projeto está sendo eficiente em custo e prazo.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-3.png)

## Índice de Desempenho de Custo(CPI) X Índice de Desempenho de Prazo(SPI)
Esses dois índices indicam a eficiência do projeto:
- CPI = EV / AC → mede o retorno do valor agregado em relação ao custo.
- SPI = EV / PV → mede a eficiência do tempo.

Valores maiores que 1 são positivos (eficiência); menores que 1 indicam problemas de desempenho.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-4.png)

## Custo Real(AC) X Valor Agregado(EV)
Compara o quanto foi gasto com o quanto foi produzido em valor.
- Se EV > AC, o projeto está sendo eficiente (entrega mais valor do que custa).
- Se EV < AC, está sendo ineficiente (gasta mais do que entrega).
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-5.png)

## Pontos Concluídos(PC) X Pontos Adicionados(PA)
Analisa a produtividade da equipe.
- PC mostra os pontos efetivamente concluídos na sprint.
- PA indica os pontos que vieram de sprints anteriores (dívida técnica).

Se PA está crescendo, é um sinal de acúmulo de tarefas pendentes. Comparar com PC ajuda a identificar se a equipe está conseguindo manter o ritmo ou está ficando sobrecarregada.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-6.png)

## Custo Real(AC) e Custo Estimado(BAC)
Essa comparação mede quanto já foi gasto (AC) em relação ao orçamento total previsto (BAC). 
- Ajuda a prever se o projeto poderá ser concluído dentro do orçamento.
- Se AC > BAC antes do fim do projeto, há um estouro orçamentário.
    Essa análise é útil para prever desvios financeiros no decorrer do projeto.
### Release 1
![release-1](../../assets/images/custo/release-1/Gerenciamento-de-custo-7.png)