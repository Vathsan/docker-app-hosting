FROM rocker/shiny:latest

# Install any R packages needed
#RUN R -e "install.packages('ggplot2', repos='http://cran.rstudio.com/')"

# Copy your app
COPY kmeans_server.R /srv/shiny-server/kmeans/server.R
COPY ui.R /srv/shiny-server/kmeans/ui.R
COPY single_file_app.R /srv/shiny-server/simple_histogram/app.R

# Ensure proper permissions
RUN chown -R shiny:shiny /srv/shiny-server

# Expose Shiny port
EXPOSE 3838