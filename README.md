# shin-thesis-code

To run the code, first download and install [Ipopt](https://coin-or.github.io/Ipopt/INSTALL.html) with HSL libraries. You need to manually compile Ipopt to run it with HSL solver library (the binary provided with Ipopt.jl will not work). Then, set the environmental variables `JULIA_IPOPT_LIBRARY_PATH` and `JULIA_IPOPT_EXECUTABLE_PATH` to point the the shared library and AMPL executable repspectively.
```
export JULIA_IPOPT_LIBRARY_PATH=/path/to/lib
export JULIA_IPOPT_EXECUTABLE_PATH=/path/to/bin
```

Now, we are ready to instantiate the project. Run the following on the repository's root directory
```
cd /path/to/shin-thesis-code
julia --project=. -e "using Pkg; Pkg.instantiate()"
```
This will install all the necessary dependencies. Finally, run
```
julia --project=. -t 20 run_case_study.jl 
```
*Note: Above script will use 20 threads!* Make sure that your machine has enough cores. If not, reduce the number of therads to a reasonable number. Enjoy!

## Questions?
Please send an email to Sungho Shin (`firstname.lastname.ss at gmail.com`)
