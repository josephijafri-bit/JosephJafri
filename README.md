## 👋 Hi, I am Joseph -

A second year Geography student at the University of Manchester, focused on geospatial data analysis and risk management. I am looking for a 2027 year-in-industry placement in flood risk, GIS or environmental data analytics.

## Projects

### Flood hazard calibration 🌊 (Ongoing Personal Project) 

Modelled Flood extent from terrain data (HAND and slope), testing how well it reproduced Environment Agency flood zones. The threshold search was automated in Python (arcpy) Within ArcGIS Pro. Data was stored and sorted in SQL to find the optimal HAND and slope values for given areas. This was then visualized in excel. Extended to a first look at property exposure by linking Land Registry sales to the flood zones.



## Results
Tested across 7 tiles, covering various terrain types:

| Tile | Terrain | AVF CSI (slope 32) |
|---|---|---|
| NY30NW (Lake District) | Upland | 0.876 |
| TL89SW (Mundford) | Flat | 0.833 |
| SK08SW (Peak District) | Upland | 0.777 |
| SD88NE (Yorkshire Dales) | Upland | 0.724 |
| SJ99NE (Stalybridge) | Urban valley | 0.532 |
| SO82SE (Gloucester) | Flat | 0.481 |
| TM59SW (Lowestoft) | Coastal | 0.120 |

<img width="1049" height="574" alt="image" src="https://github.com/user-attachments/assets/3cdc1349-f333-4f85-8ec5-c2473affe003" />

*Upland tiles keep improving with a looser threshold; coastal barely responds.*

<img width="1240" height="584" alt="image" src="https://github.com/user-attachments/assets/bc374be8-b23f-4395-a249-e467a61340b5" />

*HAND treshold is unimportant after passing a low minimum across individual tiles.*

## Housing exposure

To test the hazard layer against property, I linked Land Registry sales to
Environment Agency flood zones for the SK postcode area. Sales were placed using
postcode coordinates (ONSPD), intersected with EA Flood Zones 2 and 3, and
compared with the median house price of the area they fall in (ONS small-area
statistics).
- 30 sales fell within floodzones: 63% in Zone 3, 37% in Zone 2.
- Indicative value using area-median prices: roughly £7.1m.
- Actual value: £16.5m, with one £2.35m sale skewing average.
- 57% sold above their area's median,

**Limitations:** one month of sales (a small sample); postcode-level locations
are approximate; area medians are from an older period than the sales.

## Next steps
- Use a full year of sales for a larger sample.
- Add building counts from OS Open UPRN for density.
- Repeat across other tiles.





### Flood impacts to Gloucester Royal Hospital's functionality 🏥 (individual coursework)
Assessed how compound flood hazards affect the functionality of Gloucester Royal Hospital, using a multi-scale GIS analysis from the River Severn catchment down to individual roads and buildings. I combined LiDAR terrain data, Environment Agency flood datasets (recorded flood outlines and Risk of Flooding from Surface Water) and OS roads and buildings in QGIS, using 2 m contour analysis, elevation banding, vector overlay and zonal statistics. I found about 18 km of road across the study area within the flood extent, 70% of it A roads such as the A430 and A417. Although the hospital sits on high ground (19.3 m AOD), access would likely fail before the building itself is affected.

<img width="969" height="766" alt="image" src="https://github.com/user-attachments/assets/b4c12e7b-9d82-420d-bd0c-3013cdb01dd2" />

*Figure shows A roads within the flood extent.*


### Green infrastructure and PM2.5 in Manchester 🌳 (group project)
Investigated whether the size of a green space affects Particulate matter levels (PM2.5 µg/m<sup>3</sup>) by comparing two parks in Manchester, Platt Fields Park and Gartside Gardens. We measured PM2.5 levels at 15 randomly sampled sites per park using a grid-based method, then analysed averages, spread and correlation. Average levels were similar in both parks, but the larger park varied more. A common finding was readings near trees were higher (r=0.71), showing a strong positive correlation. This supported the hypothesis that vegetation geometry mattered more than park size. I wrote the introduction, conclusion and half the discussion, and the group peer reviewed each others work.

<img width="745" height="436" alt="Screenshot 2026-09-25 110409" src="https://github.com/user-attachments/assets/e2c97042-30f9-4b1b-998e-1bacf064bcac" />

*Figure shows an arial view of Platt Fields where the orange points display PM2.5 levels. (Made by group in ArcGIS).*



