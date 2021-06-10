# Proxyeconomics_original
Proxyeconomics Agent based model

The model is written in Python3.7 using the 'Mesa0.8.6' package. 
I used 'Anaconda' environment manager and 'spyder3.3.6' editor.
All simulations were run on a standard PC (20GB RAM).

To install Mesa:
in the Anaonda Prompt run: pip install Mesa
(note that this is case-sensitive)

You will also need the following packages, which can be installed in a similar way or using the anaconda package manager:
'matplotlib, numpy, pandas, scipy, random'

The model code is in: ProxyModel1.py

It contains two main classes (ProxyAgent, ProxyModel), defining the behavior of the agents and overall model, respectively.
Additionally it contains a number of data collector functions to compute model means used by the mesa batch_runner.

To run a family of models load and run eg.: run_ProxyModel_competition.py
Within you can set the parameters of interest:

The total number of modelsteps can be set under finalStep (line 37)
Each run_ProxyModel_....py file is made to display a family of models over one variable parameter (e.g. competition, line 38),
where the other parameters can be set within lines 39 to 48
The number of model repeats for each individual parameter constellation can be set under iterations (line51)

Default parameters in run_ProxyModel_competition are set to reproduce Fig.3,4
Fig. 5 was produced by increasing the finalStep to 10000 and the data_collect_interval (line39) to 10 
Fig. 6 was produced by running families with other variable parameters (e.g. run_ProxyModel_selection_pressure.py)
Fig. 7 was produced by modifying the get_prospect() function in the ProxyAgent class in ProxyModel1.py to ''' Step Prospect ''' (A-C)
  or by setting angle_agency (line 48 in run_ProxyModel_....py) to 1 (D-F)


