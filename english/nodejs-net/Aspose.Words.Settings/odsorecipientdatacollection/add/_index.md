---
title: OdsoRecipientDataCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "OdsoRecipientDataCollection.add method. Adds an object to the end of this collection."
type: docs
weight: 40
url: /nodejs-net/aspose.words.settings/odsorecipientdatacollection/add/
---

## add(value) {#odsorecipientdata}

Adds an object to the end of this collection.


```js
add(value: Aspose.Words.Settings.OdsoRecipientData)
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | [OdsoRecipientData](../../odsorecipientdata/) | The object to add. Cannot be ``null``. |

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

