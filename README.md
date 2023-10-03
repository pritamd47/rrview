# rrview

Interactive dashboard for visualizing river regulation due to artificial reservoirs.

To start a dashboard server, the following data is needed (1) path to compiled data, (2) points and (3) links geometry of the reservoir network

```
panel serve src/rrview/app.py --allow-websocket-origin="*" --show --args <1> -npts <2> -nlnk <3>
```

For example, this is a sample of a recent command I used to run the dashboard -
```
panel serve src/rrview/app.py --port=5100 --allow-websocket-origin="*" --show --args /water2/pdas47/2023_01_24-river-regulation/data-era5-2010_2021/regulation/regulation_data.insitu.obs_outflow.ERA5.nc -npts /water2/pdas47/2023_01_24-river-regulation/data-cumberland/cumberland_rivreg/cumberland_rivreg_pts.geojson -nlnk /water2/pdas47/2023_01_24-river-regulation/data-cumberland/cumberland_rivreg/cumberland_rivreg.geojson
```
