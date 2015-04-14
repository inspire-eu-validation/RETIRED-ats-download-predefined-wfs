# Pre-defined Stored Queries must be provided to make pre-defined datasets available

**Purpose**: 
Pre-defined Stored Queries must be provided to make pre-defined datasets available. Any possible (i.e. available) combinations of CRS/DataSetIdCode/DataSetIdNamespace/language must be made available through pre-defined stored queries. Pre-defined Stored Queries must use the parameter names 'CRS', 'DataSetIdCode', 'DataSetIdNamespace' and 'Language' to identify the CRS, dataset ID code, dataset ID namespace and language components of a query.

**Test method**

* Perform a DescribeStoredQueries-request. Test that the [DescribeStoredQueriesResponse](#DescribeStoredQueriesResponse) contains at least one [StoredQueryDescription](#StoredQueryDescription) with the [Parameters](#Parameter): '[CRS](#CRS)', '[DataSetIdCode](#DataSetIdCode)', '[DataSetIdNamespace](#DataSetIdNamespace)' and '[Language](#Language)'.
* Perform a GetFeature request with the [Stored Query ID](#storedQueryId) from the [DescribeStoredQueriesResponse](#DescribeStoredQueriesResponse), for each dataset. Obtain the parameter values for [CRS](#CRS) and [Language](#Language) in the request from the Capabilities document and the parameter values for the [DataSetIdCode](#DataSetIdCode) and [DataSetIdNamespace](#DataSetIdNamespace) from the [Metadata document(s) as referred to in the Capabilities document](#metadataDocument) or the Capabilities document. The response of the GetFeature request with the [Stored Query ID](#storedQueryId) must contain at least one feature.


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
Metadata document(s) as referred to in the Capabilities document <a name="metadataDocument"></a> | //wfs:FeatureType/wfs:MetadataURL/@xlink:href