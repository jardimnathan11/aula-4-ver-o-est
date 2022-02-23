# aula-4-ver-o-est
library(dplyr)
install.packages('raster')
library(ggplot2)
pacman::p_load(terra, spData)

my_rast = rast(file.path('C:/Users/Nathan/Downloads/brasil_coverage_2020.tif'))
plot(my_rast)
ggsave('rast 30.png')
rast120_agg = aggregate(my_rast , fact = 3)
plot(rast120_agg)
ggsave('rast 120.png')
rast990_agg = aggregate(my_rast , fact = 33)
plot(ras990t_agg)
ggsave("rast 990.png")
#as imagens nao mudaram tanto assim
