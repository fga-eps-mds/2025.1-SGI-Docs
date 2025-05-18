# Planejamento de custo - Método

# Introdução
Foram desenvolvidos e adotados por muitas equipes, nas últimas décadas, técnicas de valor agregado(EV), assim como metodologias de gerenciamento de processo.
A equipe, após pesquisar e assistir as aulas do professor Hilmer, chegou a conclusão de que a melhor maneira de calcular o custo seria utilizando os métodos do Agile EVM(Earned Value Management). Alguns conceitos que a equipe utilizará:

- Custo estimado (BAC)  
- Custo real (AC)  
- Valor planejado (PV)  
- Valor agregado (EV)  
- CPI: Cost Performance Index (Índice de Desempenho de Custos)  
- SPI: Schedule Performance Index (Índice de Desempenho de Prazo)  
- CPV: Cost Performance Variance (Variação de Desempenho de Custo)  
- SPV: Schedule Performance Variance (Variação de Desempenho de Prazo)  
- Sprints Planejadas (PS)  
- Pontos Planejados (PP)  
- Pontos Planejados da Release (PRP)  
- Custo por Sprint (SC)  
- Pontos Concluídos (PC)  
- Pontos Adicionados (PA)  
- Total de Esforço por Sprint  
- Porcentagem Real Concluída por Sprint  
- Porcentagem Planejada Concluída (PPC)  
- Porcentagem Real Concluída

## Custo estimado(BAC)

No início de um projeto é importante ter um custo de produção, pois isso facilita entender o valor do produto e a percepção do desenvolvimento do projeto ao longo do tempo. Para o cliente o valor é algo fácil de entender. Observe abaixo o custo estimado da equipe ao longo das sprints, o custo estimado é de aproximadamente **R$237.370,30**. 

<div style="position: relative; width: 100%; height: 0; padding-top: 117.4352%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https://www.canva.com/design/DAGni6PGYKg/RbKpTQgZsRIW9lUAAdsmKg/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAGni6PGYKg&#x2F;RbKpTQgZsRIW9lUAAdsmKg&#x2F;view?utm_content=DAGni6PGYKg&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">Gerenciamento de custo</a> by Jackes da Fonseca

## Custos real(AC)

O custo real representa quanto foi de fato gasto com o projeto no total ou numa sprint específica. É importante lembrar que o custo real não deve sofrer grandes variações do custo estimado e caso essa variação ocorra é preciso entender o porquê, independente se essa variação foi positiva(gastou mais do que estimou) ou negativa(gastou menos do que estimou). Essa avaliação pode trazer reflexões como:

- A ferramenta X não é utilizada pela equipe
- O gasto com o recurso Y é bem maior do que antecipado anteriormente.
- Quantidade de horas trabalhada pela equipe sofreu variações.

## Valor planejado(PV)

Essa métrica serve para entender qual o valor de cada sprint. O custo estimado leva em consideração as ferramentas, o pessoal e outros gastos que poderão ser feitos durante o projeto, porém não levam em consideração as pontuações da sprint. O valor planejado leva em consideração a quantidade total de pontos da release, quanto pontos serão feitos durante a sprint e seu valor monetário.

```bash
Valor Planejado = (Custo Estimado(BAC)/Pontos Planejados para Release(PRP)) * Pontos Planejados(PP)
```
### Exemplo utilizando a equipe

Com um planejamento de **576** pontos totais, cada ponto vale em média **R$412,10(R$237.370,30/576)** então **13** pontos valem:

```bash
Valor Planejado = R$412,10 * 13 = R$5.357,30 
```

## Valor agregado(EV)

O objetivo dessa métrica é entender o quanto a equipe avançou com o projeto em um determinado momento. O valor agregrado representa o quanto de valor foi criado até o momento. Ele será feito no final da sprint, pois é neste momento que se sabe quantos pontos foram entregues. Para calcular seu valor utilizamos a seguinte fórmula:

```bash
Valor Agregado = Porcentagem Real Concluída por Sprint(APC) * Custo Estimado(BAC)
```

## SPI: Schedule Perfomance Index (Índice de Desempenho de Prazo)

O índice de desempenho de prazo serve para entender o quanto do planejado foi entregue. Desta maneira a equipe consegue facilmente perceber atrasos observando este índice, observe a fórmula abaixo:

```bash
SPI = Valor Agregado(EV) / Valor Planejado(PV)
```
- Maior que 1: o projeto está adiantado no cronograma
- Igual a 1: o projeto está de acordo com o cronograma
- Menor que 1: o projeto está atrasado de acordo com o cronograma

## SPV: Schedule Perfomance Variance (Variação de Desempenho de Prazo)

Esse cálculo tem como objetivo informar a equipe a quantidade de trabalho que foi realizada e a quantidade de trabalho que precisa ser feita. Este cálculo observa como a sprint foi financeiramente levando em consideração apenas o valor planejado.

```bash
SPV = Valor Agregado(EV) - Valor Planejado(PV)
```

A partir do seu resultado é possível saber que:

- SPV > 0: a quantidade de trabalho que foi feito a mais e o quanto de dinheiro que ganhou.
- SPV = 0: não foi feito nenhum trabalho a mais.
- SPV < 0: a quantidade de trabalho que não foi feita e o quanto de dinheiro que perdeu.

## Custo Estimado X Custo Real

Como nem sempre o custo planejado é igual ao custo real, é necessário utilizar outras métricas que tem o mesmo objetivo porém levam em consideração o custo real.

- CPV: Cost Variance (Variação de Custo)
    - Essa variação representa o quanto de valor a sprint trouxe menos o quanto de custo a sprint teve.
```bash
CPV = Valor Agregado(EV) - Custo da Sprint(SC)
```

- CPI: Cost Performance Index (Índice de Desempenho de Custos)
    - Maior que 1: o projeto está gastando menos que o previsto
    - Igual a 1: o projeto está gastando de acordo com o previsto
    - Menor que 1: o projeto está gastando mais que o previsto
```bash
CPI = Valor Agregado(EV) / Custo da Sprint(SC)
```

## Sprints Planejadas(PS)

Quantidade de sprints que a equipe prevê até alguma release. Esse número não deve mudar, pois o tempo do projeto é limitado.

## Pontos Planejados(PP)

Quantidade de pontos planejados por sprint.

## Pontos Planejados Release(PRP)

Total de pontos que uma release tem ao somar os pontos planejados de todas as sprints se obtêm o PRP.

## Custo da Sprint(SC)

Representa qual o custo médio planejado para cada sprint.

```bash
Custo Sprint = BAC/PS
```

## Pontos Concluídos(PC)

Quantidade de pontos concluídos na sprint.

## Pontos Adicionados(PA)

Quantidade de pontos que vieram como atraso de uma sprint anterior.

```bash
    PA(n) = PA(n-1) + PP(n-1) - PC(n-1).
```
PA da sprint atual é igual à PA da sprint anterior + PP da sprint anterior - PC da sprint anterior.

## Total de Esforço Sprint

Representa a quantidade de pontos que foram realizados em relação a quantidade total de pontos que precisa ser feita.

```bash
Esforço(n) = (PP(n) + PA(n))/PC(n)
```

## Porcentagem Real Concluída por Sprint(APC)

Representa a quantidade de trabalho que foi concluída nessa sprint em relação ao trabalho total.

```bash
Porcentagem Real Concluída por Sprint = PRP/PC;
```

## Porcentagem Planejada Concluída(PPC)

Representa a quantidade de trabalho que deveria estar concluída a cada sprint. Tenta dividir o trabalho igualmente durante as sprints

```bash
PPC(n) = PP(n)/PRP;
```

## Porcentagem Real Concluída(PRC)

É semelhando ao APC, porém esta porcentagem representa todo o trabalho feito até o momento e não apenas o trabalho feito em uma sprint. Somatório de todos os APC até o momento. Então se o número da sprint = 5.

```bash
Porcentagem Real Concluída(5) = APC(1) + APC(2) + APC(3) +APC(4) + APC(5)
```
## Aplicação no projeto

<div style="position: relative; width: 100%; height: 0; padding-top: 117.4352%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https://www.canva.com/design/DAGni6PGYKg/RbKpTQgZsRIW9lUAAdsmKg/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAGni6PGYKg&#x2F;RbKpTQgZsRIW9lUAAdsmKg&#x2F;view?utm_content=DAGni6PGYKg&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">Gerenciamento de custo</a> by Jackes da Fonseca

## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 17/05/2025 | Adiciona método do planejamento de custo    | Jackes       |