---
title: OdsoRecipientData class
linktitle: OdsoRecipientData class
articleTitle: OdsoRecipientData class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.OdsoRecipientData class. Represents information about a single record within an external data source that is to be excluded from the mail merge"
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Settings/odsorecipientdata/
---

## OdsoRecipientData class

Represents information about a single record within an external data source that is to be excluded from the mail merge.
To learn more, visit the [Mail Merge and Reporting](https://docs.aspose.com/words/nodejs-net/mail-merge-and-reporting/) documentation article.




### Remarks

If a record shall be merged into a merged document, then no information is needed about that record. 
However, if a given record shall not be merged into a merged document, then the value of the unique key 
for that record shall be stored in the [OdsoRecipientData.uniqueTag](./uniqueTag/) property of this object to indicate this exclusion.




### Constructors
| Name | Description |
| --- | --- |
| [OdsoRecipientData()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [active](./active/) | Specifies whether the record from the data source shall be imported into a document when the mail merge is performed. The default value is ``true``. |
| [column](./column/) | Specifies the column within the data source that contains unique data for the current record. The default value is 0. |
| [hash](./hash/) | Represents the hash code for this record.  Sometimes Microsoft Word uses [OdsoRecipientData.hash](./hash/) of a whole record instead of a [OdsoRecipientData.uniqueTag](./uniqueTag/) value. The default value is 0. |
| [uniqueTag](./uniqueTag/) | Specifies the contents of a given record in the column containing unique data. The default value is ``null``. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Returns a deep clone of this object. |

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

