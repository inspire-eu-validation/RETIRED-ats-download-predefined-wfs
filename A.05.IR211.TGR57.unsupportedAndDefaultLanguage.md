# A.05.IR211.TGR57.unsupportedAndDefaultLanguage

**Purpose**:
Respond to unsupported language with default language for Capabilities.
If an unsupported language or no language at all is requested for by the client, the Download Service must respond with Capabilities in the [default languages](#defaultLanguage). If a client request specifies an unsupported language, or the parameter is absent in the request, all fields [Title](#title) and [Abstract](#abstract) must be provided in the service [default languages](#defaultLanguage).

**Prerequisites**

* OGC WFS 2.0.0, A.1.1 Simple WFS
* OGC WFS 2.0.0, A.1.5 HTTP GET
* [A.12.extended.capabilities](A.12.extended.capabilities.md)

**Test method**

* Perform a GetCapabilities request without the LANGUAGE-parameter. The [language of the response](#responseLanguage) of the returned Capabilities document must be equal to the [default languages](#defaultLanguage)
* Perform a GetCapabilities request with the LANGUAGE-parameter set to an unsupported value (LANGUAGE=FOO). The [language of the response](#responseLanguage) of the returned Capabilities document must be equal to the [default languages](#defaultLanguage)
* Test if all elements [Title](#title) and [Abstract](#abstract) in the Capabilities documents are identical for both Capabilities documents.

**Reference(s)**:

* TG, Req 57
* IR, Section 2.1.1

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | //*:Title
Abstract <a name="abstract"></a> | //*:Abstract
default language <a name="defaultLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
language of the response <a name="responseLanguage"></a> | /wfs:WFS_Capabilities/ows:OperationsMetadata/ows:ExtendedCapabilities/inspire_dls:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language
