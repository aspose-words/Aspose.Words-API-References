---
title: OdsoFieldMapData class
linktitle: OdsoFieldMapData class
articleTitle: OdsoFieldMapData class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.OdsoFieldMapData class. Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document"
type: docs
weight: 140
url: /nodejs-net/aspose.words.settings/odsofieldmapdata/
---

## OdsoFieldMapData class

Specifies how a column in the external data source shall be mapped to the predefined merge fields within the document.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article.




### Remarks

Microsoft Word provides some predefined merge field names that it allows to insert into a document as MERGEFIELD or 
use in the ADDRESSBLOCK or GREETINGLINE fields. The information specified in [OdsoFieldMapData](./)
allows to map one column in the external data source to a single predefined merge field.




### Constructors
| Name | Description |
| --- | --- |
| [OdsoFieldMapData()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [column](./column/) | Specifies the zero-based index of the column within an external data source which shall be mapped to the local name of a specific MERGEFIELD field. The default value is 0. |
| [mappedName](./mappedName/) | Specifies the predefined merge field name which shall be mapped to the column number  specified by the [OdsoFieldMapData.column](./column/) property within this field mapping. The default value is an empty string. |
| [name](./name/) | Specifies the column name within an external data source for the column whose  index is specified by the [OdsoFieldMapData.column](./column/) property. The default value is an empty string. |
| [type](./type/) | Specifies if a given mail merge field has been mapped to a column in the given external data source or not. The default value is [OdsoFieldMappingType.Default](../odsofieldmappingtype/#Default). |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

### See Also

* module [Aspose.Words.Settings](../)
* class [OdsoFieldMapDataCollection](../odsofieldmapdatacollection/)
* class [Odso](../odso/)

