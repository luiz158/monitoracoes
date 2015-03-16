# Sistema de Monitoramento de Ações #

## Como Executar o Programa ##

  1. Para executar o programa, clique no arquivo **monitorWeb.bat**.

## Uso da aba Monitoramento ##

  1. Nesta opção é possível verificar as grandes variações no número de negócios, volume, gaps de abertura e média aritmética de ações que não possuem normalmente este comportamento. Os tipo de alerta mostrado na coluna `Alerta` são:
    * **Alerta _Dias Média Curta_ dias** - cotação atual possui variação positiva e é maior que a média dos ultimos `Dias Média Curta` dias, possuindo mais negócios que o `Filtro Mínimo de Negócios`.Exemplo: alerta 3 dias.
    * **Alerta _Dias Média Longa_ dias** - cotação atual possui variação positiva e é maior que a média dos ultimos `Dias Média Longa` dias, possuindo mais negócios que o `Filtro Mínimo de Negócios`.Exemplo: alerta 20 dias.
    * **Alerta _GAP Abertura_** - cotação atual possui variação positiva e possui um GAP de Abertura maior que `Variação GAP Abertura`.Exemplo: GAP 5 %.
    * **Alerta _Volume_** - cotação atual possui um volume `Multiplicador Volume` vezes maior que o volume médio dos últimos `Dias Média Longa` dias. Exemplo: VOLUME 20 dias 416.32 %.
  1. Ao clicar na opção "Arquivo -> Configurar", é possível configurar os parâmetros da aplicação http://monitoracoes.googlecode.com/svn/trunk/docs/images/ExecutarPrograma/Passo_1_Monitoramento.JPG
| **Parâmetro** | **Descrição** | **Observação** |
|:---------------|:----------------|:-----------------|
|`Data Monitor`|Data que deve exibir as informações do Monitor|A data que inicia o programa é a Data Atual, para atualizar a data mostrada na tela inical deve-se realizar este processo duas vezes (**Isto será corrigido para as próximas Versões**)|
|`Dias Média Curta`|Utilizado no cálculo da média das cotações de fechamento dos ultimos _3_ pregões|Utilizado para verificar se a cotação atual já está acima da cotação média dos ultimos 3 pregões (**Valor Default é 3**)|
|`Dias Média Longa`|Utilizado no cálculo da média das cotações de fechamento dos ultimos _20_ pregões |Utilizado para verificar se a cotação atual já está acima da cotação média dos ultimos 20 pregões (**Valor Default é 20**)|
|`Filtro Mínimo de Negócios`|Filtro para não exibir ações que não tiveram no pregão corrente menos de _10_ negócios|(**Valor Default é 10**)|
|`Variação GAP Abertura (%)`|Utilizado para mostrar ações que tiveram uma variação considerável na abertura do pregrão, ou seja, GAP de Abertura a partir de _4%_|Este alerta só será mostrado nas duas primeiras horas do pregão (**Valor Default é 4%**)|
|`Multiplicador Volume`|Utilizado para mostrar ações com volume atual maior que o volume médio durante os ultimos _Dias Média Longa_ pregões, ou seja, mostra as ações que tiveram um volume negociado **4 vezes** maior que o volume médio dos ultimos 20 pregões|(**Valor Default é 4**)|



## Uso da aba Planilha ##

  1. Nesta opção é possível verificar os suportes e resistências das **ações que compõem o índice Bovespa**, disponibilizando a relação _Stop Loss_ / _Stop Gain_ de cada componente do índice.
http://monitoracoes.googlecode.com/svn/trunk/docs/images/ExecutarPrograma/Passo_2_Planilha.JPG
| **Coluna** | **Descrição** | **Observação** |
|:-----------|:----------------|:-----------------|
|`Ação`|Código da Ação|  |
|`Variação`|Variação da Ação|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG|
|`Preço`|Cotação Atual da Ação|Atualizado pelo site da [Infomoney](http://www.infomoney.com.br) com delay de 15 minutos|
|`IFR`|Índice de Força Relativa, IFR = 100-(100/ (1 + FR)), onde FR = media de ganhos / media de perdas (Considerando a média de 9 pregões)|Se for menor do que 30 (Trinta) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG, Se for entre 30 (Trinta) e 70 (Setenta) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/AZUL.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG|
|`STK %`|Estocástico Normal, considerado Período %K igual 10 e Período %D igual 3|Se for menor do que 20 (Vinte) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG, Se for entre 20 (Vinte) e 80 (Oitenta) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/AZUL.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG|
|`Topo`|Distância da Cotação Atual em relação a máxima do pregão anterior|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/AZUL.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG|
|`Fundo`|Distância da Cotação Atual em relação a mínima do pregão anterior|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/LARANJA.PNG|
|`Suportes`|Suportes da Ação fornecida pelo site da corretora [Ágora](http://www.agorainvest.com.br)|  |
|`Resistências`|Resistência da Ação fornecida pelo site da corretora [Ágora](http://www.agorainvest.com.br)|  |
|`Stop Loss 1`|Distância entre a cotação atual e o suporte 1|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/LARANJA.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG|
|`Stop Gain 1`|Distância entre a cotação atual e a resitência 1|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/AZUL.PNG|
|`Stop Loss 2`|Distância entre a cotação atual e o suporte 2|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/LARANJA.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERMELHO.PNG|
|`Stop Gain 2`|Distância entre a cotação atual e a resitência 2|Se for maior do que 0 (Zero) será http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/VERDE.PNG, caso contrário http://monitoracoes.googlecode.com/svn/trunk/docs/images/Cores/AZUL.PNG|

[Voltar](PaginaInicial.md)