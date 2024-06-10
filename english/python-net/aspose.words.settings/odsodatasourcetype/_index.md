---
title: OdsoDataSourceType enumeration
linktitle: OdsoDataSourceType enumeration
articleTitle: OdsoDataSourceType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.OdsoDataSourceType enumeration. Specifies the type of the external data source to be connected to as part of the ODSO connection information."
type: docs
weight: 130
url: /python-net/aspose.words.settings/odsodatasourcetype/
---

## OdsoDataSourceType enumeration

Specifies the type of the external data source to be connected to as part of the ODSO connection information.

The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType
enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx.




### Members

| Name | Description |
| --- | --- |
| TEXT | Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther. |
| DATABASE | Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess. |
| ADDRESS_BOOK | Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL. |
| DOCUMENT1 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeOLEDBWord. |
| DOCUMENT2 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeWorks. |
| NATIVE | Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText |
| EMAIL | Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook. |
| NONE | The type of the external data source is not specified. Possibly wdMergeSubTypeWord. |
| LEGACY | Specifies that a given document has been connected to a legacy document format supported by the producing application  Possibly wdMergeSubTypeWord2000. |
| MASTER | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| DEFAULT | Equals to [OdsoDataSourceType.NONE](./#NONE). |

### See Also

* module [aspose.words.settings](../)
* property [Odso.data_source_type](../odso/data_source_type/)

