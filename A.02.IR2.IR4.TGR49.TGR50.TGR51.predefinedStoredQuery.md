# A.02.IR2.IR4.TGR49.TGR50.TGR51.predefinedStoredQuery

**Purpose**:
Pre-defined Stored Queries must be provided to make pre-defined datasets available. Any possible (i.e. available) combinations of CRS/DataSetIdCode/DataSetIdNamespace/language must be made available through pre-defined stored queries. Pre-defined Stored Queries must use the parameter names 'CRS', 'DataSetIdCode', 'DataSetIdNamespace' and 'Language' to identify the CRS, dataset ID code, dataset ID namespace and language components of a query.

**Prerequisites**

* [A.01.TGR60.extended.capabilities](A.01.TGR60.extended.capabilities.md)

**Test method**

* Perform a DescribeStoredQueries-request. Test that the [DescribeStoredQueriesResponse](#DescribeStoredQueriesResponse) contains at least one [StoredQueryDescription](#StoredQueryDescription) with the [Parameters](#Parameter): '[CRS](#CRS)', '[DataSetIdCode](#DataSetIdCode)', '[DataSetIdNamespace](#DataSetIdNamespace)' and '[Language](#Language)'.

**Reference(s)**:

* TG, Req 49, Req 50 and Req 51
* IR, Section 2 and section 4

**Test type**:

Automated

**Notes**

TG Requirements 49, 50 and 51 together specify the use of Stored Queries to make pre-defined datasets available.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DescribeStoredQueriesResponse <a name="DescribeStoredQueriesResponse"></a> | /wfs:DescribeStoredQueriesResponse
StoredQueryDescription <a name="StoredQueryDescription"></a>| /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription
Parameter <a name="Parameter"></a>| /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter
CRS <a name="CRS"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='CRS']
DataSetIdCode <a name="DataSetIdCode"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='DataSetIdCode']
DataSetIdNamespace <a name="DataSetIdNamespace"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='DataSetIdNamespace']
Language <a name="Language"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/wfs:Parameter[@name='Language']
Stored Query ID <a name="storedQueryId"></a> | /wfs:DescribeStoredQueriesResponse/wfs:StoredQueryDescription/@id
supported CRS <a name="supportedCRS"></a> | //wfs:DefaultCRS combined with //wfs:OtherCRS
supported language <a name="supportedLanguage"></a> | //inspire_dls:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
SpatialDataSetIdentifier ID <a name="SpatialDataSetIdentifierID"></a> | //inspire_dls:ExtendedCapabilities/inspire_dls:SpatialDataSetIdentifier
SpatialDataSetIdentifier Code <a name="SpatialDataSetIdentifierCode"></a> | //inspire_dls:ExtendedCapabilities/inspire_dls:SpatialDataSetIdentifier/inspire_common:Code
SpatialDataSetIdentifier Namespace <a name="SpatialDataSetIdentifierNamespace"></a>| //inspire_dls:ExtendedCapabilities/inspire_dls:SpatialDataSetIdentifier/inspire_common:Namespace
