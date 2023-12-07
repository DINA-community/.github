# About the project
The aim of the Detection and Identification of Network Assets (DINA) project is to improve the information of the active devices and their connections in industrial networks.

Central points to achieve this goal are
- Connection to [Malcolm](https://github.com/cisagov/Malcolm),
- Cooperation with INL/CISA,
- feedback from operators and 
- further development by the community.

In order to make this easier, software is published under licenses such as Apache 2.0 or BSD.

In terms of content, the following focal points arise, which are stored in the respective repositories:

- [Source of Truth](#source-of-truth)
- [Interface for different information sources](#interface-for-different-information-sources)
- [Passive network analysis](#passive-network-analysis)
- [Active requests](#active-requests)

## [Source of Truth](https://github.com/DINA-community/DDDC-Netbox-plugin)
The asset management tool [Netbox](https://github.com/netbox-community/netbox) serves as a user interface for capturing assets. 
The ["Device Detection and Device Characterization" plugin](<Link einfügen>) is provided to enable the import of asset information from other sources (currently operator lists, Malcolm and experimental ML-procedures) into Netbox. 
This standardizes the information when assigning to the assets during the import process.
<enhance CSAF matching with link to CSAF>

## [Interface for different information sources](https://github.com/DINA-community/ot-assetmanager)
The [Asset Manager repository](<Link einfügen>) provides tools for processing data from different sources and converting it into 
a JSON data format. This data format can be imported into Netbox. The functions include:
- Processing of Malcolm data
- Processing of PCAPS
- Data enrichment using ML methods (experimental)
- Data enrichment via heuristics (planned)
- Processing of active queries (planned for end 2024)


## [Passive network analysis](https://github.com/DINA-community/ot-parsers)
There are only a few network parsers for industrial network protocols and some of those parsers do not cover the entire range of functions of the network protocols. 
This leads to a loss of information with passive network recordings. Therefore, the aim is to support more industrial protocols and increase content coverage.
<collection of parser here>

## [Active requests](https://github.com/DINA-community/ot-nmap-scritps)
Active queries make it possible to collect significantly more and more targeted information than is the case with passive network analysis. 
Therefore, this should be carried out where it can be done safely and without interfering the controls and processes. One way of doing this is to use [Nmap scripts](<Link einfügen>) 
as presented in the [repository OT-Nmap-scripts](https://github.com/DINA-community/ot-nmap-scritps).