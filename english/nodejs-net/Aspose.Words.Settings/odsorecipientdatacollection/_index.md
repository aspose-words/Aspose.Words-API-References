---
title: OdsoRecipientDataCollection class
linktitle: OdsoRecipientDataCollection class
articleTitle: OdsoRecipientDataCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.OdsoRecipientDataCollection class. A typed collection of [OdsoRecipientData](../odsorecipientdata/) To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article."
type: docs
weight: 180
url: /nodejs-net/aspose.words.settings/odsorecipientdatacollection/
---

## OdsoRecipientDataCollection class

A typed collection of [OdsoRecipientData](../odsorecipientdata/)
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article.




### Remarks




### Constructors
| Name | Description |
| --- | --- |
| [OdsoRecipientDataCollection()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#odsorecipientdata) | Adds an object to the end of this collection. |
|[ clear()](./clear/#default) | Removes all elements from this collection. |
|[ removeAt(index)](./removeAt/#number) | Removes the element at the specified index. |

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

* module [Aspose.Words.Settings](../)
* class [OdsoRecipientData](../odsorecipientdata/)
* property [Odso.recipientDatas](../odso/recipientDatas/)

