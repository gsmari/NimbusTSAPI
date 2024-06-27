
# NimbusTSAPI

NimbusTSAPI is a python3 package used for creating GraphQL queries which are then passed to NimbusTSAPI web service.
For ease of access of Time Series data against the Nimbus system.



## Install
Install through pip

~~~bash
pip install NimbusTSAPI
~~~

## Examples

~~~python
from NimbusTSAPI import NimbusTSAPI
from datetime import datetime

TSAPI = NimbusTSAPI(url="https://localhost")
fromdatetime = datetime(2024,6,1)
todatetime = datetime(2024,6,10)
tscodes = [
    "/TimeSeries.Path.MW",
    "/TimeSeries.Path.G1.MW",
    "/TimeSeries.Path.G2.MW",
]
results = TSAPI.getTSS(tscodes,fromdatetime,todatetime)
results.DataFrame()
~~~

## Authors

Gudmundur Smari Gudmundsson [gummismari@gummismari.net](mailto:gummismari@gummismari.net) -  <https://www.gummismari.net>
