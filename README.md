# how_to_add_new_julia_version_jupyter

steps to add julia versions

go to julia website

download the binary

extract it to home

remove the middle folder with hte long name, it is redunant... just have e.g. julia-1.8.0 in your home folder

use a text editor to change your ~/.bashrc $PATH variable 

then open a bash terminal

$ jupyter kernelspec  list

$ jupyter kernelspec remove julia-1.7
$ exit

then back to julia REPL

$ using Pkg; Pkg.add("IJulia")
$ Pkg.build("IJulia")

then it should turn up in your list of kernels in the notebook

also remember to add all yoru dependiceis again

in the REPL

$ using Pkg; Pkg.add("Plots")   # for example
