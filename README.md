# Utilizando MDT (Modelo Digital de Terreno do GeoSampa)

Recentemente o GeoSampa disponibilizou arquivos de MDT (Modelo digital de superfície) de toda o município de São Paulo, resultado de um sobrevoo laser (liDAr) realizado em 2017. Os arquivos, produtos desse vôo estão começando a ser disponibilizados, e como primeiro esforço os dados de MDT (Modelo digital de Terreno) estão prontos para download.

## Motivação

Buscando divulgar, estudar e formentar diversas formas de uso desse novo elemento do GeoSampa usaremos esse repositório para demonstrar algumas formas de uso, exportação e visualização desses arquivos.

## Arquivos para Download

Para fazer o dowanlod dos arquivos MDT:

* Clique em “Pesquisar”
* Aba “Download Imagens/MDC”
* Tipo “MDT”
* Selecione a(s) quadrícula(s) de interesse no mapa

![](https://raw.githubusercontent.com/geoinfo-smdu/usando-MDT/master/images/mdt-como-fazer-download.jpg)

## Utilizando o Python para processar arquivos LAZ

Acesse o [Jupyter NoteBook para acessar os arquivos LAZ por bibliotecas Python](https://github.com/geoinfo-smdu/usando-MDT/blob/master/Abrindo%20arquivo%20LAZ%20de%20MDT%20em%20Python.ipynb)

## PDAL

[PDal](https://pdal.io/) é uma biblioteca de abstração de pontos que se inspira na bilbioteca GDAL para abstração de dados raster e vetoriais. Vamos utilizar a pasta [pdal](https://github.com/geoinfo-smdu/usando-MDT/tree/master/pdal) aqui desse repositório para trabalhar alguns comandos, para tarefas básicas.