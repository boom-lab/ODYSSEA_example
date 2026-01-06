# ODYSSEA examples

Minimal examples for accessing Copernicus' ODYSSEA product.

Prerequisites: Python 3.9+ or conda (Miniconda / Anaconda)

### Quick install

#### conda
```bash
# create and activate environment
conda create -n odyssea-example python=3.10 -y
conda activate odyssea-example
```

#### pip
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Usage
See the `examples/` directory for jupyter notebooks showing how to load ODYSSEA L3S data from disk or on the fly.

To download ODYSSEA products (or any other Copernicus Marine product), we recommend using [Copernicus Marine Toolbox](https://help.marine.copernicus.eu/en/articles/7970514-copernicus-marine-toolbox-installation). 

`copernicusmarine_template/` contains a template that can be customized to download the data (subset by region and time) from the command line as:

``` sh
copernicusmarine subset --request-file copernicusmarine_template/odyssea_dl.json
```

The data is downloaded to the directory `./odyssea_data`, where the relative path `./` is from the location of execution of the command, not from the location of `odyssea_dl.json`.

Downloading Copernicus data requires (free) registration to the Copernicus Marine services, see: (https://data.marine.copernicus.eu/register).


### About ODYSSEA
- This repository demonstrates access to Copernicus' ODYSSEA product. For official documentation and datasets, see: [ODYSSEA L3S](https://data.marine.copernicus.eu/product/SST_GLO_PHY_L3S_MY_010_039/description) and the [Copernicus Marine Service](https://marine.copernicus.eu).
