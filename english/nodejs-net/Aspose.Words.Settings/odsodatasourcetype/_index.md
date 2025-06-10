---
title: OdsoDataSourceType enumeration
linktitle: OdsoDataSourceType enumeration
articleTitle: OdsoDataSourceType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.OdsoDataSourceType enumeration. Specifies the type of the external data source to be connected to as part of the ODSO connection information."
type: docs
weight: 130
url: /nodejs-net/aspose.words.settings/odsodatasourcetype/
---

## OdsoDataSourceType enumeration

Specifies the type of the external data source to be connected to as part of the ODSO connection information.

The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType
enumeration http://msdn.microsoft.com/en-us/library/bb237801.aspx.




### Members

| Name | Description |
| --- | --- |
| Text | Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther. |
| Database | Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess. |
| AddressBook | Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL. |
| Document1 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeOLEDBWord. |
| Document2 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeWorks. |
| Native | Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText |
| Email | Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook. |
| None | The type of the external data source is not specified. Possibly wdMergeSubTypeWord. |
| Legacy | Specifies that a given document has been connected to a legacy document format supported by the producing application  Possibly wdMergeSubTypeWord2000. |
| Master | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| Default | Equals to [OdsoDataSourceType.None](./#None). |

### See Also

* module [Aspose.Words.Settings](../)
* property [Odso.dataSourceType](../odso/dataSourceType/)

