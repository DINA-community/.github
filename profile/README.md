# About the project

The aim of the Detection and Identification of Network Assets (DINA) project is to improve the database of active devices and their connections in industrial networks.

Central points to achieve this goal are

- Connection to [Malcolm](https://github.com/cisagov/Malcolm),
- Cooperation with INL/CISA,
- feedback from operators and
- further development by the community.

In order to make this easier, software is published under licenses such as Apache 2.0 or BSD.

## Malcolm

In terms of content, the following focal points arise, which are stored in the respective repositories:

- [Source of Truth](#source-of-truth)
- [Interface for Different Information Sources](#interface-for-different-information-sources)
- [Passive Network Analysis](#passive-network-analysis)
- [Active Requests](#active-requests)
- [String Processing](#string-processing)

## [Source of Truth](https://github.com/DINA-community/DDDC-Netbox-plugin)

The asset management tool [NetBox](https://github.com/netbox-community/netbox) serves as a user interface for capturing assets.
The ["Device Detection and Device Characterization" plugin](https://github.com/DINA-community/DDDC-Netbox-plugin) is provided to enable the import of asset information from other sources (currently operator lists, Malcolm and experimental ML-procedures) into NetBox.
This standardizes the information when assigning to the assets during the import process. The standardized information is an important step finding matches within other data bases such as [CSAF](https://github.com/oasis-tcs/csaf).
Therefore, this feature will be improved and a CSAF-Handler will be the next step in the development.

## [Interface for Different Information Sources](https://github.com/DINA-community/ot-assetdatabase)

The [Asset Database repository](https://github.com/DINA-community/ot-assetdatabase) provides tools for processing data from different sources and converting it into
a JSON data format. This data format can be imported into NetBox. The functions include:

- Processing of Malcolm data
- Processing of PCAPS
- Data enrichment using ML methods (experimental)
- Data enrichment via heuristics (planned)
- Processing of active queries (planned)

## [Passive Network Analysis](https://github.com/DINA-community/ot-parsers)

There are not enough network parsers for industrial network protocols and some of those parsers do not cover the entire range of functions of the network protocols.
This leads to a loss of information with passive network recordings. Therefore, the aim is to support more industrial protocols and increase content coverage.
An overview of parsers can be found in the [repository OT-Parsers](https://github.com/DINA-community/ot-parsers).

## [Active Requests](https://github.com/DINA-community/ot-nmap-scritps)

Active queries make it possible to collect significantly more and more targeted information than is the case with passive network analysis.
Therefore, this should be carried out where it can be done safely and without interfering the controls and processes. One way of doing this is to use [Nmap scripts](https://nmap.org/nsedoc/scripts/) as presented in the [repository OT-Nmap-scripts](https://github.com/DINA-community/ot-nmap-scritps).

## [String Processing](https://github.com/DINA-community/string-atlas)

In order to compare different data sets or to extract information out of a string several modules are provided in the repository [String-Atlas](https://github.com/sDINA-community/string-atlas).

- string_checker
  - checking and suggesting corrections for strings
- string_miner
  - string columns are searched for possible attributes
- string_normalization
  - cleaning strings for matching
- string_synonym
  - normalizing an input string by matching it against a dictionary of given synonyms

The modules based on

- Regular expressions,
- Delete tables for prefix and suffix removal,
- Synonyms

for normalization of input data. This content is listed in the repository [String-Sysiphos](ttps://github.com/DINA-community/string-sysphos)
