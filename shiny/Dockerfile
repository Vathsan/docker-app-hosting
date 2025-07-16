FROM rocker/shiny:latest

# Install any R packages needed
RUN R -e "install.packages('ggplot2', repos='http://cran.rstudio.com/')"

# Copy your app
COPY app.R /srv/shiny-server/

# Ensure proper permissions
RUN chown -R shiny:shiny /srv/shiny-server

# Expose Shiny port
EXPOSE 3838