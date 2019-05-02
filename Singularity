Bootstrap: shub
From: CreRecombinase/docker-eigenh5

%post
    apt-get update -y -qq	
    apt-get install -y --allow-unauthenticated r-cran-tidyverse file libzmq3-dev r-cran-rsqlite
    install2.r --deps TRUE glue fs
    R -e "BiocManager::install('graph');devtools::install_github('stephenslab/ldshrink','refactor')"
    installGithub.r --deps TRUE	CreRecombinase/RSSp CreRecombinase/EigenH5@chunkreader ropensci/drake 
