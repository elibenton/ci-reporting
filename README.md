# Understanding the Claremont Independent
All the tools we used to assemble our report on the Claremont Independent's connections and influences beyond the campus boundaries.


## Our Data
## Methodologies
## Our Tools

## Setting Up the Coding Environment

##### 1. Download [Anaconda](https://www.anaconda.com/download/#macos)
##### 2. Make Project Directory

```bash
# Create project folder in desired location on computer.
mkdir Claremont-Independent-Report
cd Claremont-Independent-Report
```

##### 3. Create Virtual Environment
```bash
# Create virtual environment in which to install packages.
conda create --name ci-report

# Install all packages needed for analysis:
# - Requests
# - Beautiful Soup
# - Jupyter Lab
conda install --name ci-report requests beautifulsoup4
conda install --name ci-report -c conda-forge jupyterlab

# Activate the environment. The comand line prompt should now start with (ci-report).
source activate ci-report
```
Referece: [Setting Up a Conda Environtment](https://conda.io/docs/user-guide/getting-started.html)

##### 3. Install Mozcape Package
```bash
# Clone mozscape package from github and install the contents.
git clone https://github.com/seomoz/SEOmozAPISamples.git
cd SEOmozAPISamples/python
pip install .
```
Reference: [Mozscape API - Python Code Examples](https://github.com/seomoz/SEOmozAPISamples/tree/master/python)


##### 4. Launch Jupyter Lab
```bash
# Go back to root of project folder and launch jupyter.
cd ../..
jupyter lab
```
Reference: [Jupyter Documenation](http://jupyterlab.readthedocs.io/en/latest/getting_started/installation.html) 

##### 4. Import Necessary Libaries
```python
# Imports for python code to function properly
import pprint, os, csv, json, pickle, requests, html5lib
from bs4 import BeautifulSoup

# Import mozscape and give API credentials
from mozscape import Mozscape
client = Mozscape('my_access_id', 'my_secret_key')

# Print in format easier to read
pp = pprint.PrettyPrinter(indent=4)
```
Reference: [Mozscape API - Python Code Examples](https://github.com/seomoz/SEOmozAPISamples/tree/master/python)