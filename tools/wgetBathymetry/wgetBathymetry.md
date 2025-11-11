---
jupyter:
  jupytext:
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.18.1
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

# WGET Bathymetry

Bathymetry compilation is available via [GMRT](https://www.gmrt.org) using the [GMRT MapTool](https://www.gmrt.org/GMRTMapTool/) and from [GeoMapApp](https://www.geomapapp.org/)

Direct downloads are available programmatically using the [GMRT Webservices](https://www.gmrt.org/services/index.php) as NetCDF grid files, ESRI ASCII, or GeoTIFF. Below is a python snippet to automate URL extraction from GMRT Webservices.

# Install dependencies

```python
# (Colab and Binder users run this cell first)
!pip install -q -r https://raw.githubusercontent.com/schmidtocean/data-at-sea/main/tools/wgetBathymetry/requirements.txt
```

### GMRT NetCDF Grid via Python and WGET

```python
import wget

# bounding coordinates, NE and SW corner
NElong = 10.0
NElat = -50.0
SWlong = -10.0
SWlat = -60.0

# output filename
filename = "bathymetry_data"

# extension, usually .grd for netCDF
extension = ".grd"

# desired resolution
res="default" # low/default, med, high, max

# output file format
format="netcdf" # netcdf, esriascii, geotiff

# layer
layer="topo" # topo, topo-mask

# URL construction
url = f"http://www.gmrt.org/services/GridServer?minlongitude={SWlong}&maxlongitude={NElong}&minlatitude={SWlat}&maxlatitude={NElat}&format={format}&resolution={res}&layer={layer}"

# fetch via WGET
wget.download(url, filename+extension)

```
