# The Capabilities document contains the response language

**Purpose**: 

The Extended Capabilities shall indicate the [response language](#responseLanguage) used for the GetCapabilities-Response. Depending on the requested language the value of the [inspire_common:ResponseLanguage](#responseLanguage) corresponds to the current used language. If a [supported languages](#supportedLanguage) was requested, [inspire_common:ResponseLanguage](#responseLanguage) shall correspond to that requested language. If an unsupported language was requested or if no specific language was requested [inspire_common:ResponseLanguage](#responseLanguage) shall correspond to the service [inspire_common:DefaultLanguage](#defaultLanguage)


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