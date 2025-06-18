# About the project

The aim of the Detection and Identification of Network Assets (DINA) project is to improve the data quality of active devices and their connections in industrial networks. This is done in order to contribute to the Network Traffic Analysis Tool Suite [Malcolm](https://github.com/cisagov/Malcolm).

This repository is intended to provide a platform for the community so that, after the initial development of additional functions for Malcolm, these can be improved and further developed on the basis of user experience across company boundaries. In order to make this easier, software is published under licenses such as Apache 2.0 or BSD.

In terms of content, the following focal points arise, which are stored in the respective repositories:

- [About the project](#about-the-project)
  - [Source of truth](#source-of-truth)
  - [Interface for different information sources](#interface-for-different-information-sources)
  - [Passive network analysis](#passive-network-analysis)
  - [CSAF Handler](#csaf-handler)
  - [Active requests](#active-requests)
  - [Record linkage](#record-linkage)

## [Source of truth](https://github.com/DINA-community/DDDC-Netbox-plugin)

The asset management tool [NetBox](https://github.com/netbox-community/netbox) serves as a user interface for capturing assets.
The ["Device Detection and Device Characterization" plugin](https://github.com/DINA-community/DDDC-Netbox-plugin) is provided to enable the import of asset information from other sources (currently operator lists, Malcolm and possibly in future experimental ML-procedures) into NetBox.
This standardizes the information when assigning to the assets during the import process. The standardized information is an important step finding matches within other data bases such as [CSAF](https://github.com/oasis-tcs/csaf).
Therefore, this feature will be improved and a CSAF-Handler will be the next step in the development.

## [Interface for different information sources](https://github.com/DINA-community/devicemgt)

The [device management repository](https://github.com/DINA-community/devicemgt) provides tools for processing data from different sources and converting it into a JSON data format. This data format can be imported into NetBox. The functions include:

- Processing of Malcolm data
- Processing of PCAPS
- Data enrichment using ML methods (research area)
- Data enrichment via heuristics (e. g. MAC-addresses - in revision)
- Processing of active queries (postponed)

## [Passive network analysis](https://github.com/DINA-community/ot-parsers)

Industrial network protocols are often used for specific applications in a sector and some of these parsers do not cover the entire range of functions of the network protocols.
This leads to a loss of information with passive network recordings. Therefore, the aim is to support more industrial protocols and increase content coverage.
An overview of parsers can be found in the [repository ICSNPP-dev](https://github.com/DINA-community/icsnpp-dev).

## [CSAF Handler](https://github.com/DINA-community/DINA-community/csaf-netbox-plugin)

To determine whether assets (e.g., software, device types, or individual devices) are affected by vulnerabilities, comparison with security advisories is essential. To reduce the time required, automated matching between assets and security advisories in [CSAF](csaf.io) is supported via the [CSAF-NetBox-Plugin](https://github.com/DINA-community/csaf-netbox-plugin).

## [Active requests](https://github.com/DINA-community/ot-nmap-scritps)

Active queries make it possible to collect significantly more and more targeted information than is the case with passive network analysis.
Therefore, this should be carried out where it can be done safely and without interfering the controls and processes. One way of doing this is to use [Nmap scripts](https://nmap.org/nsedoc/scripts/) as presented in the [repository OT-Nmap-scripts](https://github.com/DINA-community/ot-nmap-scritps).

## [Record linkage](https://github.com/DINA-community/string-atlas)

In order to compare different data sets or to extract information out of a string several modules are provided in the repository [String-Atlas](https://github.com/sDINA-community/string-atlas).

The modules based on

- regular expressions,
- delete tables for prefix and suffix removal,
- synonyms

for normalization of input data. This rules and look-up tables are listed in the repository [String-Sysiphos](ttps://github.com/DINA-community/string-sysiphos)
