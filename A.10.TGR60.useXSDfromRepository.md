# The Extended Capabilities shall use the XML Schema from the INSPIRE repository.

**Purpose**: 

The [ExtendedCapabilities](#ExtendedCapabilities) must use the XML Schema as defined in the INSPIRE online schema repository.

**Test method**

* Perform a GetCapabilities request
* Validate the Capabilities document to the XML schema at http://inspire.ec.europa.eu/schemas/inspire_dls/1.0/inspire_dls.xsd.

**Reference(s)**: 

* TG, Req 60

**Test type**: 

Automated

**Notes**

The XML schema validation might be redundant, if already performed in other tests. This is an implementation choice.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/