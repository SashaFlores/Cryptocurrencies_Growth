Part 2: Will Stablecoins Eventually Provide a Better Alternative to the US Dollar?


```python
# Import Dependencies:
from pathlib import Path
import pandas as pd
# Determine the CSV Path for Bitcoin Transactions Daily:
btcdt_file = Path ('Bitcoin_Daily_Transactions.csv')
# Pass The File to Pandas and Define The Index:
btcdt_df = pd.read_csv(btcdt_file, index_col = "Date", parse_dates=True)
# Testing the DF
btcdt_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Value</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-31</th>
      <td>327789</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>346521</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>354742</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>326769</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>298580</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Rename Columns for Bitcoin Transactions Daily:
btcdt_df = btcdt_df.rename(columns= {'Value':'# of BTC Transactions Daily'})
# Testing Drops 
btcdt_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th># of BTC Transactions Daily</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-31</th>
      <td>327789</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>346521</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>354742</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>326769</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>298580</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Import Dependencies:
from pathlib import Path
import pandas as pd
# Determine the CSV Path for Bitcoin Wallets Active Daily:
btcw_file = Path ('Bitcoin_Wallets_Daily.csv')
# Pass The File to Pandas and Define The Index:
btcw_df = pd.read_csv(btcw_file, index_col = "Date", parse_dates=True)
# Testing the DF
btcw_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Value</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-31</th>
      <td>689993</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>717842</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>745966</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>690892</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>608050</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Rename Columns for Bitcoin Wallets Active Daily:
btcw_df = btcw_df.rename(columns= {'Value':'# of BTC Wallets Active Daily'})
# Testing Drops 
btcw_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th># of BTC Wallets Active Daily</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-31</th>
      <td>689993</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>717842</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>745966</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>690892</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>608050</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Import Dependencies:
from pathlib import Path
import pandas as pd
# Determine the CSV Path for Ripple:
xrp_file = Path ('XRP-USD.csv')
# Pass The File to Pandas and Define The Index:
xrp_df = pd.read_csv(xrp_file, index_col = "Date", parse_dates=True)
# Testing the DF
xrp_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Adj Close</th>
      <th>Volume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-08-01</th>
      <td>0.008438</td>
      <td>0.008441</td>
      <td>0.008220</td>
      <td>0.008222</td>
      <td>0.008222</td>
      <td>196429</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>0.008225</td>
      <td>0.008232</td>
      <td>0.008170</td>
      <td>0.008230</td>
      <td>0.008230</td>
      <td>206009</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>0.008230</td>
      <td>0.008321</td>
      <td>0.008223</td>
      <td>0.008281</td>
      <td>0.008281</td>
      <td>231262</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>0.008277</td>
      <td>0.008320</td>
      <td>0.008263</td>
      <td>0.008271</td>
      <td>0.008271</td>
      <td>178712</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>0.008264</td>
      <td>0.008286</td>
      <td>0.008221</td>
      <td>0.008224</td>
      <td>0.008224</td>
      <td>219269</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Dropping the Extra Columns in DF for Ripple:
xrp_df.drop(columns=["Open", "High", "Low", "Adj Close", "Volume"], inplace=True)
# Rename Columns for Ripple:
xrp_df = xrp_df.rename(columns= {'Close':'XRP Close'})
# Testing Drops 
xrp_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>XRP Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-08-01</th>
      <td>0.008222</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>0.008230</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>0.008281</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>0.008271</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>0.008224</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Import Dependencies:
from pathlib import Path
import pandas as pd
# Determine the CSV Path for Tether:
usdt_file = Path ('Tether-USD-5-Years.csv')
# Pass The File to Pandas and Define The Index:
usdt_df = pd.read_csv(usdt_file, index_col = "Date", parse_dates=True)
# Testing the DF
usdt_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Adj Close</th>
      <th>Volume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-07-31</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>110</td>
    </tr>
    <tr>
      <th>2015-08-01</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1765</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>4443</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>258279</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>4182</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Dropping the Extra Columns in DF for Tether:
usdt_df.drop(columns=["Open", "High", "Low", "Adj Close", "Volume"], inplace=True)
# Rename Columns for Tether
usdt_df = usdt_df.rename(columns= {'Close':'USDT Close'})
# Testing Drops 
usdt_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDT Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-07-31</th>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2015-08-01</th>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Determine CSV Path for USD Index:
usdx_file = Path('DX-Y.NYB.csv')
# Pass Market Index to Pandas and Define Index:
usdx_df = pd.read_csv(usdx_file, index_col = "Date", parse_dates=True)
# Testing the DF
usdx_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Adj Close</th>
      <th>Volume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-07-31</th>
      <td>97.470001</td>
      <td>97.599998</td>
      <td>96.309998</td>
      <td>97.370003</td>
      <td>97.370003</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>97.220001</td>
      <td>97.580002</td>
      <td>97.160004</td>
      <td>97.489998</td>
      <td>97.489998</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>97.480003</td>
      <td>98.000000</td>
      <td>97.209999</td>
      <td>97.930000</td>
      <td>97.930000</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>97.910004</td>
      <td>98.220001</td>
      <td>97.639999</td>
      <td>97.959999</td>
      <td>97.959999</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Dropping the Extra Columns in DF for USDX:
usdx_df.drop(columns=["Open", "High", "Low", "Volume", "Adj Close"], inplace=True)
# Testing Drops 
usdx_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-07-31</th>
      <td>97.370003</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>97.489998</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>97.930000</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>97.959999</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Rename Columns for USDX
usdx_df = usdx_df.rename(columns= {'Close':'USDX Close'})
# Remove NaN's
usdx_df = usdx_df.apply (pd.to_numeric, errors='coerce')
usdx_df = usdx_df.dropna()
usdx_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDX Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-07-31</th>
      <td>97.370003</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>97.489998</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>97.930000</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>97.959999</td>
    </tr>
    <tr>
      <th>2015-08-06</th>
      <td>97.830002</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Calculate Daily Close Data for Ripple:
xrp_close=xrp_df['XRP Close'].pct_change()
xrp_close.head()
```




    Date
    2015-08-01         NaN
    2015-08-02    0.000973
    2015-08-03    0.006197
    2015-08-04   -0.001208
    2015-08-05   -0.005683
    Name: XRP Close, dtype: float64




```python
# Convert the Series to a DF:
xrp_close = xrp_close.to_frame()
```


```python
# Rename Column / Drop Null:
xrp_close = xrp_close.rename(columns={'XRP Close':'XRP Daily Close'})
xrp_close.dropna(inplace=True)
# Checking Tail
xrp_close.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>XRP Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-28</th>
      <td>0.029530</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>0.055681</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>0.005854</td>
    </tr>
    <tr>
      <th>2020-07-31</th>
      <td>0.058817</td>
    </tr>
    <tr>
      <th>2020-08-01</th>
      <td>0.118287</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Calculate Daily Close Data for Tether:
usdt_close=usdt_df['USDT Close'].pct_change()
usdt_close.head()
```




    Date
    2015-07-31    NaN
    2015-08-01    0.0
    2015-08-02    0.0
    2015-08-03    0.0
    2015-08-04    0.0
    Name: USDT Close, dtype: float64




```python
# Convert the Series to a DF:
usdt_close = usdt_close.to_frame()
```


```python
# Rename Column / Drop Null:
usdt_close = usdt_close.rename(columns={'USDT Close':'USDT Daily Close'})
usdt_close.dropna(inplace=True)
# Checking Tail
usdt_close.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDT Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-27</th>
      <td>0.002229</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>-0.000243</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>0.001685</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>-0.000675</td>
    </tr>
    <tr>
      <th>2020-07-31</th>
      <td>-0.001719</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Calculate Daily Close Data for USDX:
usdx_close=usdx_df['USDX Close'].pct_change()
usdx_close.head()
```




    Date
    2015-07-31         NaN
    2015-08-03    0.001232
    2015-08-04    0.004513
    2015-08-05    0.000306
    2015-08-06   -0.001327
    Name: USDX Close, dtype: float64




```python
# Convert the Series to a DF:
usdx_close = usdx_close.to_frame()
# Rename Column / Drop Null:
usdx_close = usdx_close.rename(columns={'USDX Close':'USDX Daily Close'})
usdx_close.dropna(inplace=True)
# Checking Tail
usdx_close.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDX Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-24</th>
      <td>-0.002640</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>-0.008047</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>0.000854</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>-0.005333</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>-0.003539</td>
    </tr>
  </tbody>
</table>
</div>




```python
frames = [usdt_close, usdx_close]
combined = pd.concat(frames)
combined
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDT Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-08-01</th>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-02</th>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>0.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2020-07-24</th>
      <td>NaN</td>
      <td>-0.002640</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>NaN</td>
      <td>-0.008047</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>NaN</td>
      <td>0.000854</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>NaN</td>
      <td>-0.005333</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>NaN</td>
      <td>-0.003539</td>
    </tr>
  </tbody>
</table>
<p>3077 rows × 2 columns</p>
</div>




```python
frames = [xrp_close, usdx_close]
combined = pd.concat(frames)
combined
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>XRP Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2015-08-02</th>
      <td>0.000973</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-03</th>
      <td>0.006197</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-04</th>
      <td>-0.001208</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-05</th>
      <td>-0.005683</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2015-08-06</th>
      <td>-0.024319</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2020-07-24</th>
      <td>NaN</td>
      <td>-0.002640</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>NaN</td>
      <td>-0.008047</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>NaN</td>
      <td>0.000854</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>NaN</td>
      <td>-0.005333</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>NaN</td>
      <td>-0.003539</td>
    </tr>
  </tbody>
</table>
<p>3077 rows × 2 columns</p>
</div>



Graphs & Tables


```python
%matplotlib inline
from matplotlib import pyplot as plt
btcdt_df.plot(title="Total # of Unique BTC Daily Transactions", figsize=(20,10))
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7fb31d689550>




![png](output_23_1.png)



```python
plt.savefig('btc_transactions.png', dpi=300, bbox_inches='tight')
```


    <Figure size 432x288 with 0 Axes>



```python
%matplotlib inline
from matplotlib import pyplot as plt
btcw_df.plot(title="Total # of Unique BTC Wallets Active Daily", figsize=(20,10))
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7fb31f2f8d10>




![png](output_25_1.png)



```python
plt.savefig('btc_wallets_active.png', dpi=300, bbox_inches='tight')
```


    <Figure size 432x288 with 0 Axes>



```python
xrp_folio = pd.concat([xrp_close, usdx_close], axis='columns', join='inner')
xrp_folio.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>XRP Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-24</th>
      <td>-0.017001</td>
      <td>-0.002640</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>0.040422</td>
      <td>-0.008047</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>0.029530</td>
      <td>0.000854</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>0.055681</td>
      <td>-0.005333</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>0.005854</td>
      <td>-0.003539</td>
    </tr>
  </tbody>
</table>
</div>




```python
%matplotlib inline
xrp_folio.plot(title="XRP & USDX Close", figsize=(20,10))
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7fb31dc2f6d0>




![png](output_28_1.png)



```python
plt.savefig('xrp_usdx_close.png', dpi=300, bbox_inches='tight')
```


    <Figure size 432x288 with 0 Axes>



```python
corr=xrp_folio.corr()
corr
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>XRP Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>XRP Daily Close</th>
      <td>1.000000</td>
      <td>-0.041772</td>
    </tr>
    <tr>
      <th>USDX Daily Close</th>
      <td>-0.041772</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
usdt_folio = pd.concat([usdt_close, usdx_close], axis='columns', join='inner')
usdt_folio.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDT Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2020-07-24</th>
      <td>0.000808</td>
      <td>-0.002640</td>
    </tr>
    <tr>
      <th>2020-07-27</th>
      <td>0.002229</td>
      <td>-0.008047</td>
    </tr>
    <tr>
      <th>2020-07-28</th>
      <td>-0.000243</td>
      <td>0.000854</td>
    </tr>
    <tr>
      <th>2020-07-29</th>
      <td>0.001685</td>
      <td>-0.005333</td>
    </tr>
    <tr>
      <th>2020-07-30</th>
      <td>-0.000675</td>
      <td>-0.003539</td>
    </tr>
  </tbody>
</table>
</div>




```python
%matplotlib inline
usdt_folio.plot(title="USDT & USDX Close", figsize=(20,10))
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7fb31dbb2750>




![png](output_32_1.png)



```python
plt.savefig('usdt_usdx_close.png', dpi=300, bbox_inches='tight')
```


    <Figure size 432x288 with 0 Axes>



```python
corr=usdt_folio.corr()
corr
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>USDT Daily Close</th>
      <th>USDX Daily Close</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>USDT Daily Close</th>
      <td>1.000000</td>
      <td>0.000818</td>
    </tr>
    <tr>
      <th>USDX Daily Close</th>
      <td>0.000818</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Visualizing Daily Close Changes for Tether:
%matplotlib inline
usdt_close.plot(title="USDT Daily Close", figsize=(20,10))
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7fb31dfa8950>




![png](output_35_1.png)



```python
plt.savefig('usdt_daily_close.png', dpi=300, bbox_inches='tight')
```


    <Figure size 432x288 with 0 Axes>

