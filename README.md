# Dirt to Data
Polygon Division for Turning Dirt into Data using Quantum GIS; a Public Goods project.  Identification and GIS digitization of an IRL property in Wyoming known as "Parcel 0" AKA "Parcel Zero," the first property purchased by [CityDAO](https://www.citydao.io).

## Overview
Note that this repo has a [Companion Guide on Notion](https://danielritchie.notion.site/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7).  The Notion page has a complete breakdown of how to use the assets contained in this repository, as well as related background info such as:
 - [Deed Description & Survey Info w/PLSS Overview](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#a74f960ef33d4ff08c355bf695adfe44)
 - [Sourcing GIS Data](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#a07f902a5313499abb9c42f30951700d)
 - [Vegetation Estimation & Land Classification](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#44ba07a634a14a43894e4dc8628325c4)
 - [Identifying Additional Geospacial Features](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#f1d0ef5fefe24fe5b8252e79d5580b9b)
 - [Polygon Division (Multiple Plots from a Single Parcel)](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#7c7d5866faab425999b2ce4061ef7d1b)
 - [Assigning Metadata to Polygons](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#21e87367998d481ab677b5f16d81e1a5)
 - [Creating GeoJSON for Use in Web Apps](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#95bcbdd9f0e34ac59a81c6dd54603ef5)
  
## Datasets (/data)
Notable files are **highlighted**.
| Dataset | Description | Use |
| ----------- | ----------- | ------------- |
|OG_Parcel0 | Outdated borders| Reference Data |
|**CityDAO_ParcelZero | The foundation of this project.  Current boundaries of CityDAO.io's "Parcel Zero" AKA "Parcel 0"  | Reference Data **|
|usfs_border | USGS Forest Service boundary (entire west boundary of property)| NFT Metadata (TBD) |
|corners | Brass PLSS Corners referenced in deed, and aluminum property corners from survey| IRL Marker |
|drainage | Prominent drainage areas across property | Reserved Area |
|entrance_gate | An area reserved for a potential entrance gate to the property| Reserved Area |
|launchpad | An area reserved for a virtual rocket launching pad (or helipad) | Reserved Area |
|roads | The main access road into the property, and an old 4x4 path to the top of Moon Mountain| Reserved Area |
|rust_belt | An area of the property that appears to have a high iron content| Possible NFT Metadata |
|subdivisions | Arbitrary subdivisions around the property, to be used for metadata (Degen Valley, LFG Heights, Diamond Hill, Moon Township, tbd) | NFT Metadata (TBD) |
|TBD: Moon Mountain| The Parcel's western peak; highest point on the property | TBD |
|TBD: Diamond Hill| The Parcel's Prominent Hill, where the flag is planted | TBD |
|TBD: Plots (example only, final TBD)| A shapefile containing the divided polygons | Reference Data |
|**TBD: consolidated| | **|
|**TBD: geojson|File to be consumed by a web app, E.g. [CityDAO's Parcel Viewer](https://citydao.vercel.app/)|**|
|Google Satellite Image |||
|TBD: Avalanche Danger || NFT Metadata (TBD) |

## Images (/imagery)
| Image | Description | Use |
| ----------- | ----------- | ------ |
|Google Satellite Image |||
|**Classified Raster (Google Satellite)| Land Composition (Rock/Dirt/Vegetation) | NFT Metadata ** |

### Use Descriptions
Reference Data
Reserved Area 
NFT Metadata 
 
