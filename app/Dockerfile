FROM rocker/tidyverse

RUN apt-get update && apt-get install -y \
    libudunits2-dev\
    libgdal-dev\
    libgeos-dev\
    libproj-dev\
    libglpk-dev

RUN R -e "install.packages('lubridate')"
RUN R -e "install.packages('RPostgreSQL ')"
RUN R -e "install.packages('DT')"
RUN R -e "install.packages('pacman')"
RUN R -e "install.packages('ggplot2')"
RUN R -e "install.packages('ggthemes')"
RUN R -e "install.packages('httr')"
RUN R -e "install.packages('jsonlite')"
RUN R -e "install.packages('dplyr')"
RUN R -e "install.packages('leaflet')"
RUN R -e "install.packages('geojsonsf')"
RUN R -e "install.packages('sf')"
RUN R -e "install.packages('here')"
RUN R -e "install.packages('tinytex')"
RUN Rscript -e "tinytex::install_tinytex()"

COPY StateoftheDB.Rmd /home/rstudio/app/StateoftheDB.Rmd
COPY Makefile /home/rstudio/app/Makefile

# Running only this image - not as a Docker compose file
#docker run --rm -e PASSWORD='test' -v $PWD:/home/rstudio/app report make -C '/home/rstudio/app' all