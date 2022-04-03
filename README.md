# Web Application for an ETF Analyzer
We’ll build a financial database and web application by using SQL, Python, and the Voilà library to analyze the performance of a hypothetical fintech ETF.

Our analysis of a fintech ETF will consists of four stocks: GOST, GS, PYPL, and SQ.

Analyze the daily returns of the ETF stocks both individually and as a whole. Then deploy the visualizations to a web application by using the Voilà library.

## Technologies

Web Application for an ETF Analyzer project leverages python 3.7 with the following packages:

  [Pandas](https://github.com/pandas-dev/pandas "Pandas") 

   [SQL](https://www.w3schools.com/sql/)

   [Voila](https://github.com/voila-dashboards/voila)

## Installation Guide

First install the following libraries and dependencies.

```
# conda
conda install pandas
```

```
import numpy as np
import pandas as pd
import hvplot.pandas
import sqlalchemy
import voila
```

## Usage

**Analyze a Single Asset in the ETF**

We’ll use SQL queries with Python, Pandas, and hvPlot to analyze the performance of a PYPL asset from the ETF.


![PYPL_daily_returns](PYPL_daily_returns.png)

**Optimize Data Access with Advanced SQL Queries**

Next we’ll continue to analyze a single asset (PYPL) from the ETF. We’ll use advanced SQL queries to optimize the efficiency of accessing data from the database.


**Analyze the ETF Portfolio**

In this part, we’ll build the entire ETF portfolio and then evaluate its performance. To do so, we’ll build the ETF portfolio by using SQL joins to combine all the data for each asset.

```
query = """SELECT *
           FROM GDOT
           INNER JOIN PYPL ON
           GDOT.time = PYPL.time
           INNER JOIN GS ON
           GDOT.time = GS.time
           INNER JOIN SQ ON
           GDOT.time = SQ.time
"""
```

![ETF_cumprod](EFT_Cumprod.png)

**Deploy the Notebook as a Web Application**
We will use the Voilà library to deploy the notebook as a web application. 

![Voila Run Video](Voila.mov)

<br>Running Voila screenshots
![](Voila_1.png)
![](Voila_2.png)
![](Voila_3.png)

## Contributors

* Brought to you by Olga Koryachek.
* Email: olgakoryachek@live.com
* [LinkedIn](https://www.linkedin.com/in/olga-koryachek-a74b1877/?msgOverlay=true "LinkedIn")


---

## License

Licensed under the [MIT License](https://choosealicense.com/licenses/mit/)
