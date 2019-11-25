# Trabalhando dados LAZ com PDAL

[PDal](https://pdal.io/) é uma biblioteca de abstração de pontos que se inspira na bilbioteca GDAL para abstração de dados raster e vetoriais. Para informações completas recomendamos acessar o site, é uma biblioteca bem extensa e completa para trabalhar com nuvem de pontos.

## Juntando vários arquivos em uma pasta

Vamos inicialmente juntar quadro arquivos contidos na pasta mdts, utilizando o filtro [Merge](https://pdal.io/stages/filters.merge.html). O arquivo criado foi o `juntando_laz.json` e o comando para processa-lo:

`pdal pipeline ./juntando_laz.json`

## Convertendo um arquivo LAZ em um Modelo digital de terreno raster

Utilizando o tutorial criamos o arquivo `laz2tiff.json` para poder converter um arquivo LAZ em um raster tif seguindo o turorial [Gerando um Modelo digital de Terreno Raster com PDAL](https://pdal.io/workshop/exercises/analysis/dtm/dtm.html)
O comando portanto para rodar esse _PipeLine_ é o seguinte:

`pdal pipeline ./laz2tiff.json`

