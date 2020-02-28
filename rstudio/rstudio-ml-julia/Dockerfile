FROM cyversevice/rstudio-ml:latest

RUN sudo apt install julia

RUN julia -e 'using Pkg; Pkg.add(["Gadfly","RCall","PhyloNetworks","PhyloPlots"])'
