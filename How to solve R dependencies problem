getDependencies <- function(package_name){
  
  packages_list <- unlist(
    tools::package_dependencies(packages = package_name, db = available.packages(),
                                which = c("Depends", "Imports"),
                                recursive = TRUE))
  packages_list <- union(package_name, packages_list)
  
  return(packages_list)
}

getDependencies("tidyverse")

download.packages(pkgs = getDependencies("tidyverse"), destdir = "/home/lehlsy0904/R/x86_64-pc-linux-gnu-library/4.0")

src_pkgs <- list.files("/home/lehlsy0904/R/x86_64-pc-linux-gnu-library/4.0")
src_pkgs <- list.files(pattern = ".*tar.gz")

install.packages(src_pkgs, repos = NULL, type = "source")

install.packages('tidyverse')
