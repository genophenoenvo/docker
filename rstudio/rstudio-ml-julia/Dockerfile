FROM cyversevice/rstudio-ml:latest

RUN wget https://julialang-s3.julialang.org/bin/linux/x64/1.3/julia-1.3.1-linux-x86_64.tar.gz && \
	tar -xvzf julia-1.3.1-linux-x86_64.tar.gz && \
	cp -r julia-1.3.1 /opt/ && \
	ln -s /opt/julia-1.3.1/bin/julia /usr/local/bin/julia 

RUN julia -e 'using Pkg; Pkg.add(["CSV","DataFrames","StatsModels","Gadfly","RCall","PhyloNetworks","PhyloPlots"])'

RUN R -e 'install.packages("JuliaCall", dependencies = TRUE)'
