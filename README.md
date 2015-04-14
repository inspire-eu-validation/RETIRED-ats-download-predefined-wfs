ats-download-predefined-wfs
===========================

Abstract Test Suite for INSPIRE Download Services WFS pre-defined data-set download conformance class

References
* [INSPIRE Download Services Technical Guidance version 3.1](http://inspire.ec.europa.eu/documents/Network_Services/Technical_Guidance_Download_Services_v3.1.pdf)
* [COMMISSION REGULATION (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:02009R0976-20101228&from=EN)

*Note*: 

This ATS is in draft stage, none of the tests have an official INSPIRE MIG approval.

This Conformance Class contains the following tests:

| Identifier                                                        | Origin | Mechanical | Status   |
| ----------------------------------------------------------------- | ------ | ---------- | -------- |
| [A.01.IR2.IR4.TGR46.simpleWFS](A.01.IR2.IR4.TGR46.simpleWFS.md)    | TG     | [OGC CITE](#ogccite)        | Draft    |
| [A.02.IR3.TGR47.query](A.02.IR3.TGR47.query.md)    | TG     | [OGC CITE](#ogccite)       | Draft    |
| [A.03.TGR48.httpGet](A.03.TGR48.httpGet.md)   | TG     | [OGC CITE](#ogccite)       | Draft    |
| [A.04.IR2.IR4.TGR49.TGR50.TGR51.predefinedStoredQuery](A.04.IR2.IR4.TGR49.TGR50.TGR51.predefinedStoredQuery.md) | TG   | Yes | Draft    |
| TGR 52 | TG | No | - |


<a name="ogccite">OGC's CITE</a> tests could be used to test conformance to the WFS standard. The CITE tests is useful for several TG requirements. Information on the test can be found at [http://cite.opengeospatial.org/](http://cite.opengeospatial.org/) and more specifically at [http://cite.opengeospatial.org/teamengine/about/wfs20/2.0.0/site/index.html](http://cite.opengeospatial.org/teamengine/about/wfs20/2.0.0/site/index.html).


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
fes | http://www.opengis.net/fes/2.0
gmd | http://www.isotc211.org/2005/gmd
gml | http://www.opengis.net/gml/3.2
inspire\_common| http://inspire.ec.europa.eu/schemas/common/1.0
inspire\_dls   | http://inspire.ec.europa.eu/schemas/inspire_dls/1.0
ows | http://www.opengis.net/ows/1.1
wfs | http://www.opengis.net/wfs/2.0
xlink          | http://www.w3.org/1999/xlink