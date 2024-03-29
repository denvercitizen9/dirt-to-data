# Dirt to Data - a Public Goods Project
Turning Dirt into Data with Quantum GIS and the [RFCL Polygon Divider Plugin](https://github.com/jonnyhuck/RFCL-PolygonDivider).  Digitization of an IRL property in Wyoming known as "Parcel 0" AKA "Parcel Zero" for use in related NFTs.  Parcel Zero is the first property purchased by [CityDAO](https://www.citydao.io).

## Overview
Note that this repo has a [Companion Guide on Notion](https://danielritchie.notion.site/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7) which coveres everything that you need to know.  The Notion page has a complete breakdown of how to use the assets contained in this repository to source meaningful metadata, as well as related background info such as:
 - [Deed Description & Survey Info w/PLSS Overview](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#a74f960ef33d4ff08c355bf695adfe44)
 - [Sourcing GIS Data](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#a07f902a5313499abb9c42f30951700d)
 - [Vegetation Estimation & Land Classification](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#44ba07a634a14a43894e4dc8628325c4)
 - [Identifying Additional Geospacial Features](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#f1d0ef5fefe24fe5b8252e79d5580b9b)
 - [Automated Polygon Division (Creating Multiple Plots from a Single Parcel)](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#7c7d5866faab425999b2ce4061ef7d1b)
 - [Assigning Metadata to Polygons](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#21e87367998d481ab677b5f16d81e1a5)
 - [Creating GeoJSON for Use in Web Apps](https://www.notion.so/danielritchie/Turning-Dirt-into-NFTs-with-Quantum-GIS-4fd0479642e043739eb4beef39593bc7#95bcbdd9f0e34ac59a81c6dd54603ef5)
  
## Repository Contents   
The below identified items can be categorized into one of the following uses:  
**Reference Data** - Raw geospacial data.  May be from external sources or created from this process  
**Reserved Area** - Non-allocated; will show up as negative space against the main polygon  
**NFT Metadata** - Information extracted from the datasets for use in NFT metadata   
**Intermediary** - A compound dataset which is built from an original data source but is not yet the final output. 

Notable files are **highlighted**   

### Datasets (/data)
|DATASET|DESCRIPTION|USE|
|-----------|-----------|-----------|
|**CityDAO_ParcelZero**|Official source of the parcel boundaries; Wyoming's description of Parcel Zero|Reference Data|
|CityDAO_ParcelZero-negative|Parcel Zero, with all_negative_space removed|Intermediary|
|**CityDAO_ParcelZero-subdivided-negative**|Parcel Zero, subdivided, with all_negative_space removed.  This is the Polygon that is divided into plots.  |Intermediary|
|CityDAO_ParcelZero-subdivided|Arbitrary subdivisions around the property, to be used for metadata (Degen Valley, LFG Heights, Diamond Hill, Moon Township, Tendie Town) |NFT Metadata|
|OG_Parcel0|The original boundaries, outdated|Reference Data|
|OG_Parcel_6_complete|The original boundaries with road and parking, outdated|Reference Data|
|all_negative_space|Intermediate data source.  Combination of degentrance, drainage, roads, and launchpad (as separate objects)|Intermediary|
|all_negative_space_combined-draintop|all_negative_space, but as a single object showing drainage on top (visual for the Parcel viewer)|Intermediary|
|all_negative_space_combined-roadtop|all_negative_space, but as a single object showing roads on top (visual for the Parcel viewer)|Intermediary|
|all_negative_space_combined|Intermediate data source.  Combination of degentrance, drainage, roads, and launchpad (as a single object)|Intermediary|
|degentrance| An area reserved for a potential entrance gate to the property|Reserved Area |
|degentrance-road_combined||Intermediary|
|drainage| Prominent drainage areas across property |Reserved Area |
|roads| The main access road into the property, and an old 4x4 path to the top of Moon Mountain|Reserved Area |
|launchpad| An area reserved for a virtual rocket launching pad (or helipad) |Reserved Area |
|plots_v1|Output from Polygon divider|Intermediary|
|plots_v1-behemoths|Plots larger than the standard, non-allocated|Intermediary|
|plots_v1-centroid-data|Centers of Plots|Intermediary|
|plots_v1-compliant-allocated|Standard sized plots which were allocated to NFT holders|Intermediary|
|plots_v1-compliant|Standard sized plots|Intermediary|
|**plots_v1-final**|Consolidated file containing all metadata, assignments, and related derived info for IPFS and the Parcel Viewer|Reference Data|
|plots_v1-fragments|Plots smaller than the standard, non-allocated|Intermediary|
|plots_v1-randomized|Allocation of plots to NFT holders|Intermediary|
|points-of-interest-avalanche|Areas of risk derived from USGS 3DEP satellite data|NFT Metadata|
|points-of-interest-irl|Real POI's on the property|NFT Metadata|
|feature-areas-art|Artistic interpretations and Easter Eggs|NFT Metadata|
|feature-areas-dangers|Potential dangers on the property, not used in metadata|NFT Metadata|
|feature-areas-irl|Interesting features on the property|NFT Metadata|


### Images (/imagery)
|IMAGERY|DESCRIPTION|USE|
|-----------|-----------|-----------|
|3DEP|USGS 3D Elevation Profile Images; Lidar and IfSAR technology used to create DEM, DSM, Lidar point cloud images|Reference Data|
|3DEP-32612|Same as above, but with 32612 CRS|Reference Data|
|aspect|Output from r.slope.aspect|Intermediary|
|aspect-32612|Same as above, but with 32612 CRS|Intermediary|
|aspect-classification|Classified aspect data |NFT Metadata|
|avalanche-classification|Classified avalanche data |NFT Metadata|
|pzero_googlesat-classified_rendered|Classified Google Satellite imagery, for visually extracting Rock/Veg/Other information for each plot |NFT Metadata|
|slope|Output from r.slope.aspect|Intermediary|
|slope-32612|Same as above, but with 32612 CRS|Intermediary|
|slope-classification|Classified slope data|NFT Metadata|
|slope-classification-32612|Same as above, but with 32612 CRS|Intermediary|



### Exported Files (/output)
|OUTPUT FILE|DESCRIPTION|USE|
|-----------|-----------|-----------|
|**negative-space/all-combined.geojson**|All of the negative space features combined, used with CityDAO_ParcelZero to create CityDAO_ParcelZero-negative |Reserved Area|
|negative-space/degentrance-road_combined.geojson|Degentrance and Road, for visual layout in viewer|Intermediary|
|negative-space/degentrance.geojson|Degentrance only, for visual layout in viewer|Intermediary|
|negative-space/drainage.geojson|Drainage only, for visual layout in viewer|Intermediary|
|negative-space/launchpad.geojson|Launchpad only, for visual layout in viewer|Intermediary|
|negative-space/roads.geojson|Roads only, for visual layout in viewer|Intermediary|
|parcel/CityDAO_ParcelZero-subdivided.geojson|Subdivided Parcel |Intermediary|
|parcel/CityDAO_ParcelZero.geojson|Blank Parcel|Intermediary|
|**plots/plots_v1-IPFS.geojson**|Final/full file containing all of the plots|Reference Data|
|plots/plots_v1-ParcelViewer_Allocated.geojson|Only the plots that were allocated, used by [CityDAO's Parcel Viewer](https://citydao.vercel.app/) to separate tooltip responses|Reference Data|
|plots/plots_v1-ParcelViewer_UnAllocated.geojson|Only the plots that were unallocated, used by [CityDAO's Parcel Viewer](https://citydao.vercel.app/) to separate tooltip responses|Reference Data|


