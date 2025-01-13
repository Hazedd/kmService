<p align="center">
   <em><h1>kmService</h1></em>
</p>

[![build](https://github.com/Hazedd/kmService/workflows/Build/badge.svg)](https://github.com/Hazedd/kmService/actions)
[![codecov](https://codecov.io/gh/Hazedd/kmService/branch/master/graph/badge.svg)](https://codecov.io/gh/Hazedd/kmService)
[![PyPI version](https://badge.fury.io/py/kmService.svg)](https://badge.fury.io/py/kmService)

---

**Documentation**: <a href="https://open-imx.github.io/kmService/" target="_blank">https://open-imx.github.io/kmService/</a>

**Source Code**: <a href="https://github.com/open-imx/kmService" target="_blank">https://github.com/open-imx/kmService/</a>

**PyPi**: <a href="https://pypi.org/project/kmService/" target="_blank">https://pypi.org/project/kmService/</a>

---

The dutch rail infrastructure utilizes kilometer measurements to pinpoint the location of objects along the linear infrastructure.
This service aims to give you reference information from km and geocodes.

## Location Determination and Accuracy Disclaimer

<strong>While every effort has been made to ensure accuracy, it is important to note that location-based services are subject to inherent limitations and uncertainties.
Therefore, users are advised to use the provided location information cautiously and not solely rely on it for critical decision-making purposes.
We cannot guarantee the absolute accuracy or completeness of the data and hereby disclaim any warranties, express or implied, regarding its reliability or fitness for a particular purpose.

By utilizing this application and its location-based features, users acknowledge and accept the inherent limitations and uncertainties associated with location determination.</strong>

## Open-IMX Initiative
This open source project is part of the **Open-IMX initiative**. This initiative aims to provide a collaborative environment for developers, data analysts and railway professionals to effectively work with IMX data.

### 🗪 Discord Community Channel

💥 We invite you to join the [👉 open-imx community on Discord](https://discord.gg/wBses7bPFg).

### Features
- ✅ get actual km data from arcgis feature service
- ✅ correct hm raai to hm points
- ✅ get geocode info by xy
- ✅ get km measure and ribbon by xy
- ✅ km measure and ribbon as imx string (IMXv1-v12)

### Backlog and Issues
- backlog/roadmap and progress see [https://github.com/orgs/open-imx/projects/6](https://github.com/orgs/open-imx/projects/6)
- issues see [https://github.com/open-imx/kmService/issues](https://github.com/open-imx/kmService/issues)


## Install

```batch
pip install kmService
```

## Usage

```py

async def async_example():
    from kmService import KmService

    km_service_instance = await KmService.factory()
    return km_service_instance

def sync_example():
    from kmService import get_km_service

    # we use the get_km_service methode, and use async in the background 🎉
    km_service_instance = get_km_service()
    return km_service_instance

response = km_service_instance.get_km(x, y)
print(response.display)
print(response.geojson_string())
```

### This project is depends on the following awesome stuff!
- **Shapely**: <a href="https://pypi.org/project/shapely/" target="_blank">https://pypi.org/project/shapely/</a>
- **arcGisFeatureCache**: <a href="https://pypi.org/project/arcGisFeatureCache/" target="_blank">https://pypi.org/project/arcGisFeatureCache/</a>
- **pyproj** <a href="https://pypi.org/project/pyproj/" target="_blank">https://pypi.org/project/pyproj/</a>
- **rtree** <a href="https://pypi.org/project/Rtree/" target="_blank">https://pypi.org/project/Rtree/</a>
- **nest_asyncio** <a href="https://pypi.org/project/nest-asyncio/" target="_blank">https://pypi.org/project/nest-asyncio/</a>
- **mkdocs-material** <a href="https://pypi.org/project/mkdocs-material/" target="_blank">https://pypi.org/project/mkdocs-material/</a>
- **mkdocstrings** <a href="https://pypi.org/project/mkdocstrings/" target="_blank">https://pypi.org/project/mkdocstrings/</a>

## License

This project is licensed under the terms of the MIT license.
