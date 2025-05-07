---
title: OdsoRecipientDataCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "OdsoRecipientDataCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /nodejs-net/aspose.words.settings/odsorecipientdatacollection/count/
---

## OdsoRecipientDataCollection.count property

Gets the number of elements contained in the collection.


```js
get count(): number
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
* class [OdsoRecipientDataCollection](../)

