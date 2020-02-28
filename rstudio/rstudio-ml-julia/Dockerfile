FROM cyversevice/rstudio-ml:latest

RUN sudo apt install julia

RUN julia -e 'using Pkg; Pkg.add(["CSV","DataFrames","StatsModels","Gadfly","RCall","PhyloNetworks","PhyloPlots"])'

RUN R -e 'install.packages("JuliaCall", dependencies = TRUE)'
