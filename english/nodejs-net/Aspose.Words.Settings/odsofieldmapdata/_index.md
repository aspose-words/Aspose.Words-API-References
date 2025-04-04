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

### Examples

Shows how to access the collection of data that maps data source columns to merge fields.

```js
let doc = new aw.Document(base.myDir + "Odso data.docx");

// This collection defines how a mail merge will map columns from a data source
// to predefined MERGEFIELD, ADDRESSBLOCK and GREETINGLINE fields.
let dataCollection = doc.mailMergeSettings.odso.fieldMapDatas;
expect(dataCollection.count).toEqual(30);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.getEnumerator())
{
  int index = 0;
  while (enumerator.moveNext())
  {
    console.log(`Field map data index ${index++}, type \"${enumerator.current.type}\":`);

    console.log(
      enumerator.current.type != aw.Settings.OdsoFieldMappingType.Null
        ? `\tColumn \"${enumerator.current.name}\", number ${enumerator.current.column} mapped to merge field \"${enumerator.current.mappedName}\".`
        : "\tNo valid column to field mapping data present.");
  }
}

// Clone the elements in this collection.
expect(dataCollection.at(0).clone()).not.toEqual(dataCollection.at(0));

// Use the "RemoveAt" method elements individually by index.
dataCollection.removeAt(0);

expect(dataCollection.count).toEqual(29);

// Use the "Clear" method to clear the entire collection at once.
dataCollection.clear();

expect(dataCollection.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Settings](../)
* class [OdsoFieldMapDataCollection](../odsofieldmapdatacollection/)
* class [Odso](../odso/)

