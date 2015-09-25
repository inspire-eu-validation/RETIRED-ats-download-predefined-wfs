# A.08.IR223.TGR59.provideDefaultLanguage

**Purpose**: The Capabilities document must contain the default language.

**Prerequisites**

* [A.12.extended.capabilities](A.12.extended.capabilities.md)

**Test method**

* Check that the [DefaultLanguage](#defaultLanguage) exists. If so, pass the test. Otherwise fail the test.

**Reference(s)**:

* TG, Req 59
* IR, Section 2.2.3

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DefaultLanguage <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
