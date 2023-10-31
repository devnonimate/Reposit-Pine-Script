# Negociação de algoritmo Grid Spot

Modelo de negociação em grade para negociação algorítmica.

O código lançado é escrito na linguagem Pine Script para Trading View (versão 5). O script é configurado como uma estratégia, dando a você a capacidade de fazer backtest em todos os mercados. Você pode facilmente transformá-lo em um indicador removendo as funções de entrada e saída do mercado.

Esta é uma estratégia longa apenas para ativos à vista.

# COMO FUNCIONA
A negociação em grade é uma estratégia de negociação em que um investidor cria uma chamada “grade de preços”. A ideia básica da estratégia é comprar repetidamente ao preço pré-especificado e depois esperar que o preço suba acima desse nível e depois vender a posição (e vice-versa com operações a descoberto ou cobertura).

![Esquema 2022-09-05 alle 20 12 16](https://user-images.githubusercontent.com/100917872/188499241-48b30ff8-4b87-42f7-a4cc-aee1bbe30ebd.png)

# CARACTERÍSTICAS
1) Grades: Este algoritmo possui um total de 10 grades.
2) Take Profit: O trader pode aumentar ou diminuir a distância entre as grades a partir do painel User Interface, a distância entre uma grade e outra representa o Take Profit.
3) Gestão: O algoritmo compra 10% do capital cada vez que o preço rompe uma grade e vende durante uma subida para a próxima grade superior. O capital inicial é investido em 10 tamanhos que representam 10% do capital por negociação.
4) Stop Loss: O algoritmo não conhece stop loss desde que não seja ativado no painel da interface do usuário. Ao ativar o stop loss no painel da interface do usuário, o algoritmo inserirá uma condição de fechamento em todas as negociações que serão calculadas a partir da última grade inferior.
6) Negociações: As negociações são abertas somente se o preço estiver dentro da grade. Se o mercado sair da grade, o algoritmo não comprará novas posições nem venderá novas posições.
7) Condições ideais de mercado: O mercado favorável para este algoritmo é o mercado lateral.

# LIMITAÇÃO DO MODELO
O trader deve levar em consideração que se trata de um modelo estático. Só funciona perfeitamente bem se o mercado estiver numa tendência lateral e incorrer em pesadas perdas se o mercado seguir uma tendência de baixa. O modelo é inutilizável para uma tendência de alta. O trader deve, portanto, analisar cuidadosamente o mercado onde pretende utilizar esta estratégia, certificando-se de que o preço apresenta uma tendência lateral.

# USOS
Ferramenta indispensável de pesquisa e backtesting para quem usa bots em seus investimentos. O algoritmo produz um backtesting da estratégia para o histórico passado. É usado por traders profissionais para entender se esta estratégia tem sido lucrativa no mercado e quais parâmetros usar para bots que usam esta estratégia (Kucoin, Binance etc.).


# CONFIGURAR
1) Copie o código
2) Cole o código no console do editor Pine
3) Salvar
4) Rodar
