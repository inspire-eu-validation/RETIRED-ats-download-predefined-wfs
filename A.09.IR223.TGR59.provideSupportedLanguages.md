# The Capabilities document contains the list of supported language

**Purpose**: 

The [ExtendedCapabilities](#ExtendedCapabilities) must contain the [list of supported languages](#listOfSupportedLanguages) indicated in <inspire_common:SupportedLanguages>. This [list of supported languages](#listOfSupportedLanguages) must consist of exactly one element [inspire_common:DefaultLanguage](#defaultLanguage) indicating the service [default language](#defaultLanguage) and zero or more elements <inspire_common:SupportedLanguage> to indicate all additional [supported language](#supportedLanguage). Regardless of the [language of the response](#responseLanguage), the [list of supported languages](#listOfSupportedLanguages) is invariant for each GetCapabilities-Response.


**Test method**

* Perform a GetCapabilities request without the LANGUAGE-parameter. Test if there is exactly one [default languages](#defaultLanguage)
* For each [supported language](#supportedLanguage), perform a GetCapabilities request with the LANGUAGE-parameter set to that [supported language](#supportedLanguage). The [language of the response](#responseLanguage) of the returned Capabilities document must be equal to the requested [supported language](#supportedLanguage). The [list of supported languages](#listOfSupportedLanguages) is the same for each request.

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
inspire_common:DefaultLanguage /  default language <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
inspire_common:ResponseLanguage <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
supported language <a name="supportedLanguage"></a>| in //wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/*/inspire_common:Language
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/
list of supported languages <a name="listOfSupportedLanguages"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages