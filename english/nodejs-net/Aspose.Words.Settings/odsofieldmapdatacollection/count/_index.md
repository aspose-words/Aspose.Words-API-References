---
title: OdsoFieldMapDataCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "OdsoFieldMapDataCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /nodejs-net/aspose.words.settings/odsofieldmapdatacollection/count/
---

## OdsoFieldMapDataCollection.count property

Gets the number of elements contained in the collection.


```js
get count(): number
```

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

* module [Aspose.Words.Settings](../../)
* class [OdsoFieldMapDataCollection](../)

