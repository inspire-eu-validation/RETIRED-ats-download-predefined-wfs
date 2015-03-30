# Implementations shall conform to ISO 19142 Conformance Class 'Query'

**Purpose**: 

Implementations shall conform to ISO 19142 Conformance Class 'Query'

**Test method**

Perform OGC CITE tests on WFS/FES

AND/OR ?

* Perform GetCapabilities request
* test if the [Constraint ImplementsQuery](#implementsquery) is present in the Capabilities document

**Reference(s)**: 

* TG, Req 47
* IR, Section 3
* ISO19143 standard, Annex A.1

**Test type**: 

Automated / defered to OGC CITE tests

**Notes**

Question: defer to OGC Cite test OR create a separate test for INSPIRE?

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Constraint ImplementsQuery <a name="implementsquery"></a> | //fes:Constraint[@name='ImplementsQuery' and ./ows:DefaultValue='TRUE']
