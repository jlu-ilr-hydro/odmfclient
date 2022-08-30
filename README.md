# API client for ODMF

This package allows programatic access to ODMF databases with Python. 
It is based on [requests](https://pypi.org/project/requests/). Data analyses in R use [the httr module](https://cran.r-project.org/web/packages/httr/vignettes/quickstart.html) 

## Installation

Missing setup.py, installation not yet working

    pip install https://github.com/jlu-ilr-hydro/odmfclient/archive/master.zip


## Usage

~~~~~~~~~~py
from odmfclient import login
with login('https://path/to/odmf', 'user', 'password') as api:
    print(api)
    # Get all datasets at site #1 with valuetype 1
    datasets = api.dataset.list(site=1, valuetype=1)
    # Get values for the first dataset found as pandas.DataFrame
    df = api.dataset.values_parquet(dsid=datasets[0])
~~~~~~~~~~
