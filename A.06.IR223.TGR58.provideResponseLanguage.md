# A.06.IR223.TGR58.provideResponseLanguage

**Purpose**: The Capabilities document must contain the response language

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET
* [A.12.extended.capabilities](A.12.extended.capabilities.md)

**Test method**

* Perform a GetCapabilities request without the LANGUAGE-parameter. The [language of the response](#responseLanguage) of the returned Capabilities document must be equal to the [default languages](#defaultLanguage)
* Perform a GetCapabilities request with the LANGUAGE-parameter set to a [supported languages](#supportedLanguage). The [language of the response](#responseLanguage) of the returned Capabilities document must be equal to the [supported languages](#supportedLanguage).

**Reference(s)**:

* TG, Req 58
* IR, Section 2.2.3

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
inspire_common:DefaultLanguage <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
inspire_common:ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
supported language <a name="supportedLanguage"></a>| in //wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/*/inspire_common:Language
