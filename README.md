# Retiredge

This repo contains the Portfolio Optimization feature of Retiredge, implemented and annoated through Python and Jupyter Notebooks. 


## Installation

The code sample can be viewed directly through github without any installation.
However, to modify and edit the file, jupyter notebook is needed. 

```bash
pip install jupyterlab
```

## Usage
The methods and functions can be used on a variety of financial datasets, which can be imported locally with the following code inside the notebook.

```python
df = pd.read_csv('ETFG_FUND.csv')
```

Alternatively, data can be retrieved from financial platforms such as Quandl. Which can be installed and used with the code:

```bash
pip install quandl
```

An API key can be retrieved for free through creating an account on Quandl.

```python
import quandl

quandl.ApiConfig.api_key = '##################'
stocks = ['ETFG/ANLT']
data = quandl.get_table('WIKI/PRICES', ticker = stocks,
                        qopts = { 'columns': ['date', 'ticker', 'adj_close'] },
                        date = { 'gte': '2016-1-1', 'lte': '2017-12-31' }, paginate=True)
```

## Contributing
Pull request are not welcome as this is a final class project.
