---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.1'
      jupytext_version: 1.2.3
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

```python
import pandas as pd
import numpy as np
import statsmodels.api as sm
from statsmodels.tsa.api import VAR
```

```python
import datetime as dt
```

```python
data = pd.read_pickle("./data.pkl")
```

```python
data_stocks = data[['AAPL','MSFT','AMZN']]
```

```python
data_stocks = data_stocks[:100]
```

```python
model = VAR(data_stocks)
```

```python
results = model.fit(3)
```

```python
results.summary()
```

```python
cov = results.forecast_cov
```

```python
cov
```

```python

```
