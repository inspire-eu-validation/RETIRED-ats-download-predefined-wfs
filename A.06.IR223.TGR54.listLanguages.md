# Download Service provides supported languages

**Purpose**: 

The Download Service must provide a list of [supported languages](#supportedLanguages) in the [ExtendedCapabilities](#ExtendedCapabilities) section.

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd
* Test if the [ExtendedCapabilities](#ExtendedCapabilities) section contains a list of [supported languages](#supportedLanguages), with at least one language.

**Reference(s)**: 

* TG, Req 54
* IR, Section 2.2.3

**Test type**: 

Automated

**Notes**

The XML schema validation might be redundant, if already performed in other tests. This is an implementation choice. If this is not done, the third step (explicit testing for the list of supported languages) must at least be done.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
supported languages <a name="supportedLanguages"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages