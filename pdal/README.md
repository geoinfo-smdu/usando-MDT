# Trabalhando dados LAZ com PDAL

[PDal](https://pdal.io/) é uma biblioteca de abstração de pontos que se inspira na bilbioteca GDAL para abstração de dados raster e vetoriais. Para informações completas recomendamos acessar o site, é uma biblioteca bem extensa e completa para trabalhar com nuvem de pontos.

## Juntando vários arquivos em uma pasta

Vamos inicialmente juntar quadro arquivos contidos na pasta mdts, utilizando o filtro [Merge](https://pdal.io/stages/filters.merge.html). O arquivo criado foi o `juntando_laz.json` e o comando para processa-lo:

`pdal pipeline ./juntando_laz.json`

## Convertendo um arquivo LAZ em um Modelo digital de terreno raster

Utilizando o tutorial criamos o arquivo `laz2tiff.json` para poder converter um arquivo LAZ em um raster tif seguindo o turorial [Gerando um Modelo digital de Terreno Raster com PDAL](https://pdal.io/workshop/exercises/analysis/dtm/dtm.html)
O comando portanto para rodar esse _PipeLine_ é o seguinte:

`pdal pipeline ./laz2tiff.json`

## Abrindo o arquivo no qGis

Agora que temos o arquivo raster `tiff` podemos importa-lo para o qGis e visualizarmos o terreno 3D.
![](https://raw.githubusercontent.com/geoinfo-smdu/usando-MDT/master/images/terreno3d.PNG)

## Cratera de Colônia

A cidade de São Paulo tem um patrimônio geológico importante, a cratera de Colônia. No Brasil existem apenas 5 estruturas como essa e apenas 70 no mundo todo. Sendo que a de São Paulo a mais próxima de um ambiente urbano.
Não a toa vamos utilizar a cratera de Colônia para experimentar um processamento de dados Lidar.
Primeiramente é necessário baixar os dados MDT do site do [GeoSampa](http://geosampa.prefeitura.sp.gov.br/) conforme a imagem:

![](https://raw.githubusercontent.com/geoinfo-smdu/usando-MDT/master/images/cratera-de-colonia.PNG)

Com os arquivos baixados e descompactados agora é necessário prcessa-los. 

Optamos por fazer isso em um processo único criando o arquivo `cratera-colonia.json` Ele junta todos os arquivos LAZ, e depois os transforma em um Raster Tiff para podermos processa-lo em qGis. Basta executar o comando:

`pdal pipeline ./cratera-colonia.json`

O resultado possibilita imagens como essas:

![](https://raw.githubusercontent.com/geoinfo-smdu/usando-MDT/master/images/createra-colonia-3d.png)