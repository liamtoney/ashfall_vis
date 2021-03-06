# Interactive visualization of ash deposition forecasts

🚨 **This repository is no longer actively maintained.** 🚨

![](demonstration.gif "Demonstration of interactive ash deposition map")

The spatial distribution, amount, and arrival time of deposited ash following a volcanic eruption are important parameters for hazard preparation and mitigation. In New Zealand, [GNS Science](https://www.gns.cri.nz/) has collaborated with [MetService](http://www.metservice.com/national/home) to modify [HYSPLIT](https://ready.arl.noaa.gov/HYSPLIT.php) &mdash; an airborne ash dispersion modeling program &mdash; for ash deposition forecasting. This repository illustrates the variety of ashfall forecast products that can be produced from the model output.

## How to navigate this repository
Your first stop should be [`concept_portfolio.ipynb`](concept_portfolio.ipynb). This Jupyter notebook showcases and explains the three most fundamental interactive visualization products included in this repository:

* An ash deposition map
* An ash thickness time profile plotting tool
* A GIS / Google Earth data export utility

It also provides an overview of some key Python tools for geovisualization. To run (and edit!) cells within the notebook, you can launch an interactive version by clicking on the badge provided in the following section.

The [`experiments/`](experiments) directory contains additional Jupyter notebooks which explore the "plotting tool space."

[`18042918_taupo_15.0_0.01.nc`](18042918_taupo_15.0_0.01.nc) is typical of the netCDF files output by the modified HYSPLIT program. This specific file describes the ashfall forecast for an eruption of the Taupō volcano on April 29th, 2018 at 18:00 NZST, with a plume height of 15 km and an erupted volume of 0.01 cubic km. The file is provided courtesy of MetService.

[`vis_tools.py`](vis_tools.py) contains several functions used within the Python code of the repository's notebooks.

You can click on the badge below to access a [nbviewer](https://nbviewer.jupyter.org/)-rendered version of this repository:

[![nbviewer](https://github.com/jupyter/design/blob/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.jupyter.org/github/liamtoney/ashfall_visual/tree/master/)

## Interactive Jupyter notebooks
Click on the badge below to access a fully executable, editable version of this repository:

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/liamtoney/ashfall_visual/master)

(Note: If you see `Waiting for build to start...` at the top of the build logs, please be patient. Constructing the binder environment takes some time.)

## Installation and dependencies
See [`environment.yml`](environment.yml) for a list of dependencies.

To create an environment with all of the dependencies installed (using [conda](https://conda.io/docs/)), run the following:
```
conda env create -f environment.yml
```
. . . then activate the environment:
```
source activate ashfall_visual
```
. . . and install a new IPython kernel to use with your Jupyter notebook:
```
pip install kernda --no-cache
python -m ipykernel install --name ashfall_visual
kernda -o -y /usr/local/share/jupyter/kernels/ashfall_visual/kernel.json
```
(Note: The path to `kernel.json` may differ for your system.)

## References
Chai, C., Ammon, C. J., Maceira, M., & Herrmann, R. B. (2018). Interactive visualization of complex seismic data and models using Bokeh. *Seismological Research Letters*, *89*(2A), 668–676. <https://doi.org/10.1785/0220170132>

Hurst, T., & Davis, C. (2017). Forecasting volcanic ash deposition using HYSPLIT. *Journal of Applied Volcanology*, *6*(1), 1-8. <https://doi.org/10.1186/s13617-017-0056-7>

Mastin, L. G., Randall, M. J., Schwaiger, H. F., & Denlinger, R. P. (2013). *User's guide and reference to Ash3d: A three-dimensional model for Eulerian atmospheric tephra transport and deposition* ([Open-File Report 2013-1122](https://pubs.usgs.gov/of/2013/1122/pdf/ofr20131122.pdf)). Reston, VA: U.S. Geological Survey.

Thompson, M. A., Lindsay, J. M., & Leonard, G. S. (2017). [More than meets the eye: Volcanic hazard map design and visual communication](https://doi.org/10.1007/11157_2016_47). In C. Fearnley et al. (Eds.), *Observing the Volcano World: Volcano Crisis Communication* (pp. 1-20). Berlin: Springer International.

</br>
<p align="center">
  <a href="https://www.gns.cri.nz">
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSKWLxovJe1WHtgvBgX08YS7vcl8HcMg2tsGCm9v5YvcodG20m2" height="70"></a>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <a href="http://www.metservice.com/national/home">
    <img src="http://m.metservice.com/sites/all/themes/mobile/images-new/hi/MetService-hammerhead-logo.svg" height="40"></a>
</p>
