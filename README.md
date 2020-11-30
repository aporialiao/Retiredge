# Retiredge

This repo contains the Portfolio Optimization feature of Retiredge, implemented and annoated through Python and Jupyter Notebooks. It also contains a 
sample ETF data retrieved from Quandl, which will be used as sample for our predictive. Lastly an image is included as the Mobile GUI prototype to
give insight on our final application.
The process utlizes Efficient Frontier Calculation to suggest optimized portfolio budget allocations for users. The process is efficient and requires
minimal financial knowledge to understand, perfect for our target market of college students.

## Purpose and Intergration
The goal of this implementation is to show how data analysis and machine learning algorithms can be feasible performed on financial datasets to help 
our users make informed decisions. There are many spaces open for modification and additional intergrations, some potential additions include:
 Markup : - Personalization 
              - Through Machine Learning on the User history and Financial information
                  - The investment style of a user (aggressive or conservative)
                  - The user perference for certain funds/stocks
                  - The degree of freedom in final portfolio decisions (how much the user relies on the ML predictions)
          - Diversivied Prediction
              -   Including more diverse data for prediction and analysis
                  - This includes data beyond market data: e.g. Social data through News and other Media
                  - Unsupervized learning can be performed on these datasets to identify more hidden trends

In terms of integrating with the actual application, only a small fraction of the displayed information will be included in the GUI through the Portfolio 
Recommendation interface. Much of the functionalities and processes will be hidden to the user for a more streamlined and friendly experience. However,
even with a simple user interface, an incredible amount of backend analysis can be performed for an optimzed investing experience. 



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
