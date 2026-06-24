---
title: "Acquiring Vector Datasets from Data Repositories"
teaching: 30
exercises: 30
---

:::::::::::::::::::::::::::::::::::::: questions

- What kinds of vector data already exist online and where can I find them?
- How do I evaluate whether a dataset is accurate, current, and appropriate for my needs?
- How do I download and bring external vector data into QGIS?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Distinguish between collecting original data and using pre-existing data from repositories
- Identify appropriate data sources for different geographic and thematic needs
- Evaluate a dataset's quality, accuracy, and fitness for purpose by examining its metadata
- Download vector datasets from public repositories and load them into QGIS

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- Pre-existing vector datasets are available from government portals, academic repositories, and open-source platforms — you rarely need to create data from scratch.
- Always examine a dataset's metadata before using it: understand when it was created, how it was collected, and what its limitations are.
- Open-access datasets vary widely in quality and completeness; exploring the data carefully is as important as finding it.
- OpenStreetMap provides a rich, continuously updated global dataset accessible both as downloads and through QGIS plugins like QuickOSM.
- Bookmark sources relevant to your research area — a curated list of trusted repositories saves significant time at the start of future projects.

::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction: Original Data vs. Pre-Existing Data

An important decision at the start of any geospatial project — whether you are making a basic reference map or conducting advanced spatial analysis — is whether you need to collect original data or whether suitable data already exists.

**Original data collection** is appropriate when:
- No existing dataset covers the geographic area or time period you need
- The precision or accuracy requirements of your project exceed what publicly available data provides
- You are documenting something that has not been mapped before

**Pre-existing data** is appropriate when:
- The feature type you need (political boundaries, road networks, river systems, populated places, etc.) has already been digitized and made available by a government agency, research institution, or open-source community
- Time or resources do not permit original data collection
- You need a large geographic extent — for example, country-level or global coverage

For most common geographic features, pre-existing data exists somewhere on the web and does not need to be recreated. Knowing where to find it, and how to evaluate its quality, is one of the most practical skills a GIS practitioner can develop.

---

## Evaluating Data Quality

Before using any dataset in your project, take time to examine it critically. Open-access datasets vary widely in quality, precision, currency, and the amount of preprocessing required before they are useful. Key questions to ask:

- **When was it created or last updated?** A road network dataset from 2005 may be unreliable for current analysis.
- **How was it collected?** Was it digitized from satellite imagery? Surveyed in the field? Derived from crowd-sourced contributions? Each method carries different accuracy expectations.
- **What is the spatial resolution or scale?** A dataset designed for 1:1,000,000 global mapping will look imprecise if zoomed to the neighborhood level.
- **What do the attribute fields represent?** Read the metadata and data dictionary — field names are often cryptic codes that need interpretation.
- **Are there known gaps or limitations?** Most reputable data providers document these in their metadata pages.

As a rule: **explore the data before you use it.** Load it into QGIS, open the attribute table, check the geographic coverage, and compare it against a basemap or another source before building analysis or a finished map on top of it.

---

## Data Source Directory

The following sections organize free, publicly accessible vector data sources by category. Sources specific to your local area (city, county, or state open data portals) are not listed here but are worth bookmarking — search for `[your city or state] open data GIS`.

::::::::::::::::::::::::::::::::::::: callout

For our next part of this session, check out the shared google doc [here](https://drive.google.com/drive/folders/1I5Rr3TaLPu4EHz8Bfe_3HKNPrzYwzL7B). Go to `Day 1 Session 1a: Vector Data/QGIS` to find resources that we will be using in our upcoming modules!

::::::::::::::::::::::::::::::::::::::::::::::::

This list is provided as a reference only; we do not guarantee the accuracy or timeliness of any individual dataset.

---

### Data Consortiums and Hubs

These platforms aggregate datasets from multiple providers and are a good starting point when you are not sure which specific source to use.

| Source | Description |
|---|---|
| [Esri Open Data Hub](https://hub.arcgis.com/search) | A large, searchable collection of open datasets contributed by government agencies and organizations worldwide. Datasets are downloadable in shapefile, GeoJSON, and other formats. |
| [NYU Spatial Data Repository](https://geo.nyu.edu/) | A curated academic geospatial repository maintained by New York University Libraries. Strong coverage of urban and international datasets. |
| [GeoPortal at Tufts](https://geodata.tufts.edu/) | Tufts University's geospatial data repository, with strong coverage of historical and international data. |
| [Big Ten Academic Alliance Geoportal](https://geo.btaa.org/) | A collaborative geoportal maintained by Big Ten universities, aggregating geospatial data from government and academic sources across North America. |
| [Demographic and Health Surveys (DHS) Spatial Repository](https://spatialdata.dhsprogram.com/home/) | Spatial data tied to DHS survey results, covering health indicators across low- and middle-income countries. |

---

### OpenStreetMap

OpenStreetMap (OSM) is a collaborative, open-license global map built by volunteers. It is one of the richest freely available sources of detailed, up-to-date geographic data, particularly for urban features.

| Source | Description |
|---|---|
| [openstreetmap.org](https://www.openstreetmap.org/) | The main OSM website. You can browse the map, contribute edits, and learn about the project. |
| [Geofabrik Downloads](https://download.geofabrik.de/) | Pre-packaged OSM data downloads organized by country and region, available in Shapefile and other common GIS formats. Best for downloading a whole country or region. |
| [OSM Map Features Wiki](https://wiki.openstreetmap.org/wiki/Map_features) | The reference guide to OSM's tagging system — explains how features like roads, buildings, land use, and amenities are classified and coded. Essential reading before running QuickOSM queries. |
| [Humanitarian OpenStreetMap Team (HOT)](https://www.hotosm.org/en/) | A nonprofit that activates OSM mapping in response to humanitarian crises. Provides curated datasets for disaster-affected areas. |

---

### Government Data Sources

Most government data portals provide data specific to their jurisdiction. The sources below cover a range of U.S. scales — city, county, federal — as well as a few of the most useful thematic federal datasets.

**City and regional portals** (most major cities have something comparable):

| Source | Description |
|---|---|
| [Open Indy Data Portal](https://data.indy.gov/) | Indianapolis's open data platform, typical of what major U.S. cities provide. |
| [City of Chicago Open Data Portal](https://data.cityofchicago.org) | One of the most comprehensive U.S. city open data portals, with hundreds of datasets on crime, health, transit, zoning, and more. |
| [City of Boston Open Data Portal](https://bostonopendata-boston.opendata.arcgis.com) | Boston's geospatial open data, including parcels, neighborhoods, and public infrastructure. |
| [NYC Planning Department Datasets](https://www.nyc.gov/content/planning/pages/resources#datasets) | New York City Department of City Planning data including zoning, land use, and administrative boundaries. |

**Federal U.S. sources:**

| Source | Description |
|---|---|
| [US Census Bureau Data and Maps](https://www.census.gov/data.html) | The primary source for demographic, economic, and boundary data for the United States. Includes TIGER/Line shapefiles for census geographies at all levels. |
| [National Historical GIS (NHGIS)](https://www.nhgis.org/) | Historical U.S. census data and boundary files from 1790 to the present, maintained by the University of Minnesota. Invaluable for temporal analysis. |
| [US HUD Geospatial Data Storefront](https://hudgis-hud.opendata.arcgis.com/) | Housing and Urban Development spatial data including fair market rents, opportunity zones, and public housing locations. |
| [US CMS Provider Data Portal](https://data.cms.gov/provider-data/datasets) | Healthcare provider locations and quality metrics from the Centers for Medicare and Medicaid Services. |
| [US County Health Rankings and Roadmaps](https://www.countyhealthrankings.org/explore-health-rankings) | Annual county-level health outcome and health factor rankings for all U.S. counties. Tabular data linkable to Census boundary files. |
| [USDA Economic Research Service, County-Level Data](https://www.ers.usda.gov/data-products/county-level-data-sets/) | Agricultural, economic, and food environment indicators at the U.S. county level. |

---

### Global Peace, Health, and Economic Well-Being

These sources provide indicators relevant to global comparative research and humanitarian applications.

| Source | Description |
|---|---|
| [DHS Program Spatial Data Repository](https://spatialdata.dhsprogram.com/home/) | Geospatial data linked to Demographic and Health Survey results across low- and middle-income countries. |
| [University of Gothenburg Quality of Government (QoG) Portal](https://www.gu.se/en/quality-government/qog-data) | Cross-national governance, corruption, and institutional quality indicators compiled from dozens of sources. |
| [Vision of Humanity — Global Peace Index](https://www.visionofhumanity.org/maps/) | Annual country-level peace and conflict indicators with interactive and downloadable maps. |
| [Uppsala Conflict Data Program (UCDP)](https://ucdp.uu.se/encyclopedia) | Maintained by Uppsala University; one of the most comprehensive databases of organized violence and armed conflict globally. |
| [WHO Global Health Observatory](https://www.who.int/data/gho) | World Health Organization data on disease burden, health system capacity, and mortality globally. |
| [World Bank World Development Indicators](https://databank.worldbank.org/source/world-development-indicators) | Comprehensive development data covering 200+ countries across economics, education, health, and environment. |
| [Maddison Project Database (University of Groningen)](https://www.rug.nl/ggdc/historicaldevelopment/maddison/releases/maddison-project-database-2020) | Long-run historical GDP and population estimates for countries worldwide, going back centuries. |
| [Freedom House — Freedom in the World](https://freedomhouse.org/report/freedom-world) | Annual assessments of political rights and civil liberties for countries and territories. |

---

### Physical and Environmental Features

| Source | Description |
|---|---|
| [Natural Earth](https://www.naturalearthdata.com/) | A public domain dataset of natural and cultural features at 1:10m, 1:50m, and 1:110m scales. Ideal for world and continental maps. Covers coastlines, rivers, lakes, country boundaries, populated places, and much more. |
| [HydroSHEDS](https://www.hydrosheds.org/) | High-resolution hydrological data derived from NASA SRTM elevation data, including river networks, watersheds, and drainage basins. |

---

::::::::::::::::::::::::::::::::::::: discussion

### Evaluating Data Sources

- You found two datasets covering the same topic from different providers. They do not agree — features that appear in one are missing from the other, or the boundaries differ. How do you decide which to trust?
- When would you choose to download a full country dataset from Geofabrik rather than running a QuickOSM query? What are the trade-offs?
- Think about the research or mapping work you want to do. Which two or three sources from the directory above are most relevant to your area of interest, and why?

::::::::::::::::::::::::::::::::::::::::::::::::