﻿---
title: OdsoRecipientData.active property
linktitle: active property
articleTitle: active property
second_title: Aspose.Words for Node.js
description: "OdsoRecipientData.active property. Specifies whether the record from the data source shall be imported into a document when the mail merge is performed"
type: docs
weight: 20
url: /nodejs-net/aspose.words.settings/odsorecipientdata/active/
---

## OdsoRecipientData.active property

Specifies whether the record from the data source shall be imported into a document when the mail merge is performed.
The default value is ``true``.



```js
get active(): boolean
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

