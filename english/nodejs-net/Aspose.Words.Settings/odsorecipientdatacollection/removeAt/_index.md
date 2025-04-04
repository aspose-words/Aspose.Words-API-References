---
title: OdsoRecipientDataCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for Node.js
description: "OdsoRecipientDataCollection.removeAt method. Removes the element at the specified index."
type: docs
weight: 60
url: /nodejs-net/aspose.words.settings/odsorecipientdatacollection/removeAt/
---

## removeAt(index) {#number}

Removes the element at the specified index.


```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero-based index of the element. |

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

