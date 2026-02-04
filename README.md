This repository contains the code for the manuscript "*Training-domain gaps in data-driven ocean color algorithms*" under review at Geophysical Research Letters.

Authors: Patrick Clifton Gray<sup>\*,1</sup>, Charlotte Begouen Demeaux<sup>1</sup>, Alison Chase<sup>2</sup>, Robert Frouin<sup>3</sup>, Emmanuel Boss<sup>\1</sup> 

1. School of Marine Sciences, University of Maine, Orono, ME, USA
2. Applied Physics Laboratory, University of Washington, Seattle, WA, USA
3. Scripps Institution of Oceanography, La Jolla, CA, USA

*Corresponding authors: Patrick Gray (patrick.gray@maine.edu)

Abstract: Bio-optical algorithms serve a critical role, enabling satellite-based monitoring of the global ocean and its ecosystems. These largely empirical algorithms invert satellite measurements of water leaving reflectance (“ocean color”) to biogeochemical parameters such as chlorophyll a, but often fail to generalize beyond their training data, leading to increased uncertainty when extrapolated. We present a simple geometric approach for assessing bio-optical model domain using a convex hull. We find that large swaths of the ocean are not within the domain of existing bio-optical models, particularly in oligotrophic gyres, but also across seasons and locations, becoming more pronounced as input dimensionality increases. Understanding those limitations and biases is critical in a changing ocean. Our work provides an interpretable metric that points to specific regions and times that should be flagged in the short-term and sampled in the long-term, with the hope of better understanding the ocean’s ecological and biogeochemical diversity.

## Code access
The notebooks included here:
1.  `exploring_modis_insitu_space.ipynb` builds convex hulls in 2 and 3D using Valente and analyzes PACE and MODIS data using this geometry.
2.  `convex_hull_seasonality.ipynb` builds a convex hull using Valente and analyzes a full year of global PACE data to inspect trends and means.
3.  `algo_bias_estimates.ipynb` builds a convex hull using the NOMAD dataset to exactly match the NASA chlorophyll-a algorithm and compares the error when predictions are made beyond the convex hull. Some supplemental figures comparing Valent and NOMAD are also made.

All python code can be run on Docker and a matching environment can be obtained by running `docker pull TBD`

# Data Access
All data is included either in this repository in the data directory (e.g. the SO-PACE and formatted Valente data) or pulled from NASA using `earthaccess` and code in the files above precisely specifies pulling this exact data.