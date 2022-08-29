FROM rocker/tidyverse
WORKDIR /code

RUN install2.r --error \
lubridate \
RPostgreSQL \
DT \
ggplot2 \
ggthemes \
httr \
jsonlite \
dplyr \
leaflet \
geojsonsf \
sf

COPY StateoftheDB.Rmd StateoftheDB.Rmd
CMD ['Rscript -e "rmarkdown::render('StateoftheDB.Rmd')"']

