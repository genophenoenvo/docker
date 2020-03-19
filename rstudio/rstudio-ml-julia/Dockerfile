FROM cyversevice/rstudio-ml:latest

RUN apt-get -y install libudunits2-dev
RUN apt-get -y install libgdal-dev
RUN apt-get -y install  libproj-dev

RUN wget https://julialang-s3.julialang.org/bin/linux/x64/1.3/julia-1.3.1-linux-x86_64.tar.gz && \
	tar -xvzf julia-1.3.1-linux-x86_64.tar.gz && \
	cp -r julia-1.3.1 /opt/ && \
	ln -s /opt/julia-1.3.1/bin/julia /usr/local/bin/julia

RUN julia -e 'using Pkg; Pkg.add(["CSV","DataFrames","StatsModels","Gadfly","RCall","PhyloNetworks","PhyloPlots"])'

RUN R -e 'install.packages("JuliaCall", dependencies = TRUE)'
RUN R -e 'install.packages("udunits2",dependencies = TRUE)'
RUN R -e 'install.packages("rgdal", dependencies = TRUE)'
RUN R -e 'devtools::install_github("r-quantities/units", dependencies = TRUE)'
RUN R -e 'devtools::install_github("usa-npn/rnpn", dependencies = TRUE)'
RUN R -e 'devtools::install_github("khufkens/phenor", dependencies=TRUE)'
RUN R -e 'install.packages("phenocamr", dependencies = TRUE)'
RUN R -e 'install.packages("maps", dependencies = TRUE)'
