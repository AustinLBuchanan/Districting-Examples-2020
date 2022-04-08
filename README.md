# Districting-Examples-2020
Examples on how to generate political districting plans. All codes are written using Python, with NetworkX used for handling graphs, Gurobi used as MIP solver, and GeoPandas used to draw maps. Used in an undergraduate Operations Research course at Oklahoma State University (IEM 4013). This repo uses 2020 Census data, while an [older repo](https://github.com/AustinLBuchanan/Districting-Examples) used 2010 data.

# The MIPs
The MIP models are summarized in [Two_districting_models.pdf]().

# The Data
TODO

The input data is typically read using the GerryChain package. It can sometimes be difficult to install GerryChain. Here is a [tutorial video](https://www.youtube.com/watch?v=_SmR2IkIt38) if you run into problems.

# The Codes
[D1-Min-Deviation.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize population deviation
  - check if the resulting districts are connected (using NetworkX)
   
[D2-Min-Cut-Edges.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize cut edges
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D3-Min-Cut-Edges-with-Contiguity.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize cut edges
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

[D4-Min-Perimeter-with-Contiguity.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties and their populations
  - build a MIP model in Gurobi to minimize total perimeter length of the districts
  - add the contiguity constraints of [Hojny et al. (MPC, 2021)](https://link.springer.com/article/10.1007/s12532-020-00186-3)
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas

[D5-Min-Moment-of-Inertia.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties, their populations, and their lat-long coordinates
  - build a MIP model in Gurobi to minimize moment of inertia
  - read a shapefile with GeoPandas
  - draw the districting plan on a map with GeoPandas
  
[D6-Min-Moment-of-Inertia-with-Contiguity.ipynb]() shows how to:
  - read a graph from a .json file (using the GerryChain reader)
  - print the names of the counties, their populations, and their lat-long coordinates
  - build a MIP model in Gurobi to minimize moment of inertia
  - add the contiguity constraints of Shirabe ([2005](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1538-4632.2005.00605.x) and [2009](https://journals.sagepub.com/doi/abs/10.1068/b34104)). See [Oehrlein and Haunert, 2017](http://www.josis.org/index.php/josis/article/viewArticle/379) and [Validi et al., 2020](http://www.optimization-online.org/DB_HTML/2020/01/7582.html) for more details.
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
  
