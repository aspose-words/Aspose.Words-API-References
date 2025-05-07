---
title: OdsoRecipientData.column property
linktitle: column property
articleTitle: column property
second_title: Aspose.Words for Node.js
description: "OdsoRecipientData.column property. Specifies the column within the data source that contains unique data for the current record"
type: docs
weight: 30
url: /nodejs-net/aspose.words.settings/odsorecipientdata/column/
---

## OdsoRecipientData.column property

Specifies the column within the data source that contains unique data for the current record.
The default value is 0.


```js
get column(): number
```

### Examples

Shows how to access the collection of data that designates which merge data source records a mail merge will exclude.

```js
let doc = new aw.Document(base.myDir + "Odso data.docx");

let dataCollection = doc.mailMergeSettings.odso.recipientDatas;

expect(dataCollection.count).toEqual(70);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.getEnumerator())
{
  int index = 0;
  while (enumerator.moveNext())
  {
    console.log(
      `Odso recipient data index ${index++} will {(enumerator.current.active ? `" : "not ")}be imported upon mail merge.");
    console.log(`\tColumn #${enumerator.current.column}`);
    console.log(`\tHash code: ${enumerator.current.hash}`);
    console.log(`\tContents array length: ${enumerator.current.uniqueTag.length}`);
  }
}

// We can clone the elements in this collection.
expect(dataCollection.at(0).clone()).not.toEqual(dataCollection.at(0));

// We can also remove elements individually, or clear the entire collection at once.
dataCollection.removeAt(0);

expect(dataCollection.count).toEqual(69);

dataCollection.clear();

expect(dataCollection.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [OdsoRecipientData](../)

