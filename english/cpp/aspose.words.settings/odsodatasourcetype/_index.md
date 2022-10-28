---
title: OdsoDataSourceType
second_title: Aspose.Words for C++ API Reference
description: Specifies the type of the external data source to be connected to as part of the ODSO connection information.
type: docs
weight: 222
url: /cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Specifies the type of the external data source to be connected to as part of the ODSO connection information.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | 0 | Specifies that a given document has been connected to a text file. Possibly wdMergeSubTypeOther. |
| Database | 1 | Specifies that a given document has been connected to a database. Possibly wdMergeSubTypeAccess. |
| AddressBook | 2 | Specifies that a given document has been connected to an address book of contacts. Possibly wdMergeSubTypeOAL. |
| Document1 | 3 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Specifies that a given document has been connected to another document format supported by the producing application. Possibly wdMergeSubTypeWorks. |
| Native | 5 | Specifies that a given document has been connected to another document format native to the producing application. Possibly wdMergeSubTypeOLEDBText. |
| Email | 6 | Specifies that a given document has been connected to an e-mail application. Possibly wdMergeSubTypeOutlook. |
| None | 7 | The type of the external data source is not specified. Possibly wdMergeSubTypeWord. |
| Legacy | 8 | Specifies that a given document has been connected to a legacy document format supported by the producing application Possibly wdMergeSubTypeWord2000. |
| Master | 9 | Specifies that a given document has been connected to a data source which aggregates other data sources. |
| Default | n/a | Equals to **None**. |


The OOXML specification is very vague for this enum. I guess it might correspond to the WdMergeSubType enumeration [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).


