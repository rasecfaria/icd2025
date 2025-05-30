# icd2025
Projeto Final da cadeira de Introdução à Ciência dos Dados




MaiorQuantidadeVendida = MAXX(SUMMARIZE(Vendas, Vendas[Data Venda], "Total", SUM(Vendas[Quantidade Vendida])), [Total])

MenorQuantidadeVendida = MINX(SUMMARIZE(Vendas, Vendas[Data Venda], "Total", SUM(Vendas[Quantidade Vendida])), [Total])

MaiorReceita = 
MAXX(
    ADDCOLUMNS(
        VALUES(Vendas[Data Venda]),
        "ReceitaPorData", 
        CALCULATE(SUMX(Vendas, Vendas[Quantidade Vendida] * Vendas[Preço Unitário]))
    ),
    [ReceitaPorData]
)

MaiorReceita = 
MAXX(
    ADDCOLUMNS(
        VALUES(Vendas[Data Venda]),
        "ReceitaPorData", 
        CALCULATE(SUMX(Vendas, Vendas[Quantidade Vendida] * Vendas[Preço Unitário]))
    ),
    [ReceitaPorData]
)

