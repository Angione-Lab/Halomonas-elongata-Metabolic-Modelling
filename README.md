# _Halomonas elongata_ Metabolic Modelling
Enuh et al., "Genome-scale metabolic modelling derived flux analysis in _Halomonas elongata_ 153B explains polyhydroxyalkanoates and ectoine biosynthesis"

This repository contains the genome-scale metabolic network model for _H. elongata_ in XML format. The model can be used to study the metabolic capabilities of this organism and perform various analyses. Below are instructions on how to use the XML model and run some analyses.


**Requirements**

To run the XML model, you need a software tool that supports reading and analyzing SBML (Systems Biology Markup Language) files, such as the COBRApy package for Python users, or the COBRA toolbox for Matlab users.

If you do not have the COBRApy package installed, you can run the code below in Python to install it:
`pip install cobra` 

Import the package:
`import cobra`


**Analysis**

Load the H.elongata_model11.xml file
`model = cobra.io.read_sbml_model("H.elongata_model11.xml")`

Run Flux balance analysis 
`solution = model.optimize()`
`print(solution)fba_solution = flux_analysis.optimize_minimal_flux(model)`

Further specific analyses can be run by following the documentation: https://cobrapy.readthedocs.io/en/latest/simulating.html
