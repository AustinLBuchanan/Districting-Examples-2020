# Districting-Examples-2020
Examples on how to generate political districting plans. All codes are written using Python, with NetworkX used for handling graphs, Gurobi used as MIP solver, and GeoPandas used to draw maps. Used in an undergraduate Operations Research course at Oklahoma State University (IEM 4013). This repo uses 2020 Census data, while an [older repo](https://github.com/AustinLBuchanan/Districting-Examples) used 2010 data. Video [lectures are available on YouTube](https://www.youtube.com/playlist?list=PLKQ1MjSFuxKdf3gtPmH5VC93f6FvDrr8R).

# The MIPs
The MIP models are summarized in [Two_districting_models.pdf](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/Two_districting_models.pdf).

# The Data
This data was obtained from the Redistricting Data Hub, and processed by Daryl DeFord to create the graphs (.json files). If you would like graphs for other states besides Oklahoma, please send me an email. The graphs are read using the GerryChain package. It can sometimes be difficult to install GerryChain. Here is a [tutorial video](https://www.youtube.com/watch?v=_SmR2IkIt38) if you run into problems.

The shapefiles are taken from [Eugene Lykhovyd's page](https://lykhovyd.com/files/public/districting/), which has data for all states (2010 and 2020). You can download all of his files using my [data downloaders](https://github.com/AustinLBuchanan/data-downloader/blob/main/eugene-data-downloader-2020.ipynb).

# The Codes
[D1-Min-Deviation.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D1-Min-Deviation.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize population deviation
  - check if the resulting districts are connected (using NetworkX)
   
[D2-Min-Cut-Edges.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D2-Min-Cut-Edges.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize cut edges
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D3-Min-Cut-Edges-with-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D3-Min-Cut-Edges-with-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - build a MIP model in Gurobi to minimize cut edges
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

[D4-Min-Perimeter-with-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D4-Min-Perimeter-with-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - build a MIP model in Gurobi to minimize total perimeter length of the districts
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

[D5-Min-Moment-of-Inertia.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D5-Min-Moment-of-Inertia.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties, their populations, and their lat-long coordinates
  - build a MIP model in Gurobi to minimize moment of inertia
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D6-Min-Moment-of-Inertia-with-Contiguity.ipynb](https://github.com/AustinLBuchanan/Districting-Examples-2020/blob/main/D6-Min-Moment-of-Inertia-with-Contiguity.ipynb) shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - build a MIP model in Gurobi to minimize moment of inertia
  - add the contiguity constraints of Shirabe ([2005](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1538-4632.2005.00605.x) and [2009](https://journals.sagepub.com/doi/abs/10.1068/b34104)). See [Oehrlein and Haunert, 2017](http://www.josis.org/index.php/josis/article/viewArticle/379) and [Validi et al., 2022](https://pubsonline.informs.org/doi/abs/10.1287/opre.2021.2141) for more details.
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

# Past Student Projects

Here are some examples of student projects from the Spring 2021 semester of IEM 4013:
  - [Idaho](https://github.com/KyleHumphreys/IEM-4013-Idaho-Districting)
  - [Nebraska](https://github.com/Jay-dnn/4013-Final-Report)
  - [Iowa](https://github.com/Jared-Johnson294/Redisctricing-Iowa)
  - [Alabama](https://github.com/livey2021/LEWVEYZAL-IEM4013-Group-Project)
  - [New Mexico](https://github.com/nathan-whitehead/New-Mexico-Redistricting-Plan)
  - [Kansas](https://github.com/William-Jackson-Ricky/Kansas-Redistricting-for-Dr.-Buchanan)
  
Here are some examples of student projects from the Spring 2022 semester of IEM 4013:
  - [Nebraska](https://github.com/KeeganJC/Nebraska)
  - [Arkansas](https://github.com/logandavis2518/IEM4013_2020RedistrictingProject)
  - [Kansas](https://github.com/hopebrittanyy/Kansas-Redistricing-OR-4013-Project-)
  - [Alabama](https://github.com/blrodgers26/IEM-4013-Final-Project)
  - [West Virginia](https://github.com/CGroenteman/OperationsResearchProject-West-Virginia-)
