# [Semana 3](https://bit.ly/Semana3_Alura) - Alura Challenge BI

## Dashboard Operacional

Nesta última semana do desafio a Alura Store disponibilizou um banco de dados da área financeira da empresa e requisitou um relatório com 2 páginas: a primeira com um *overview* financeiro e a segunda com uma área para a análise de hipóteses.

## Base de Dados

A empresa disponibilizou 4 tabelas em formato de banco de dados SQL do MySQL:

  - Tabela notas fiscais
  - Tabela produtos
  - Tabela vendedores
  - Tabela pedidos

### Relacionamentos

Há 3 relacionamentos entre as tabelas:
  
1. A 'Tabela vendedores' se relaciona com a 'Tabela notas fiscais' pela coluna 'id_vendedor', com uma cardinalidade de 1 para muitos (1:n)
2. A 'Tabela pedidos' se relaciona com a 'Tabela notas fiscais' pela coluna 'id_pedido', com uma cardinalidade de 1 para 1 (1:1)
3. A 'Tabela produtos' se relaciona com a 'Tabela pedidos' pela coluna 'id_pedidos', com uma cardinalidade de 1 para muitos (1:n)

### Tratamento de dados

  Ao analisar os dados, percebeu-se que as tabelas estavam com algumas particularidades e que estas poderiam trazer informações incorretas para o que foi requisitado. As tabelas 'Tabela notas fiscais' e 'Tabela produtos' traziam o algarismo 0 repetido nas colunas 'Valor' e 'Frete'(Tabela notas fiscais) e 'Preço' e 'Custos'(Tabela produtos). Para resolver isso, os valores das colunas foram dividios por 100 e assim a anomalia foi resolvida.
  
  Houve também um problema com a 'Tabela vendedores': havia um vendedor duplicado, gerando 2 ids diferentes (3 e 6). Para isso, foi retirada a duplicidade de informações, e, na 'Tabela nostas fiscais', foram alterados os valores de 'id_vendedor' de 6 para 3. Nesta tabela também haviam nomes com caracteres a mais, fazendo-se assim, uma limpeza desses textos.


## Métricas

Para a primeira página do relatório, foram desenvolvidas as seguintes métricas:
  
  - Despesas totais: valor total gasto em frete e em impostos
  - Lucro total: valor da receita, subtraindo as despestas e os custos
  - Custo total: custo total de produção dos itens vendidos
  - Receita total: valor recebido das compras
  
  Com essas métricas, foi pedido para que se mostrasse mensalmente as mesmas, assim como uma seleção de ano na página. Além disso, também foram criados 2 filtros para a página, o primeiro para filtrar as informações por categoria do produto e o segundo para filtrar as informações por vendedor.

Na segunda página do relatório estão as análises de cenário, onde se pode visualizar o que acontece com cada métrica desenvolvida com uma alteração percentual nas mesmas.

Além do pedido, também foi criada uma tercira página, que mostra ranking de produtos e vendedores, de acordo com o valor total vendido e também com a quantidade total vendida. São mostrados nessa página os 5 maiores resultados para cada caso.

  
## Ferramentas utilizadas
  Para a criação do dashboard foi utilizado o Microsoft Power BI. Para a criação da paleta de cores foi utilizado o [Coolors](https://coolors.co)
  
  ### Fontes dos ícones:
  
  Os ícones foram baixados do site [Icon Finder](https://www.iconfinder.com):

  [Essentials icon set](https://www.iconfinder.com/iconsets/essentials-9) produzido por [Alice Rizzo](https://www.iconfinder.com/AliceR) - Sob licensa Creative Commons (Attribution 3.0 Unported)


