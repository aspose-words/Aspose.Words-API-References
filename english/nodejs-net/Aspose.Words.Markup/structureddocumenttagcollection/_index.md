---
title: StructuredDocumentTagCollection class
linktitle: StructuredDocumentTagCollection class
articleTitle: StructuredDocumentTagCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Markup.StructuredDocumentTagCollection class. A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range"
type: docs
weight: 180
url: /nodejs-net/aspose.words.markup/structureddocumenttagcollection/
---

## StructuredDocumentTagCollection class

A collection of [IStructuredDocumentTag](../istructureddocumenttag/) instances that represent the structured document tags in the specified range.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of structured document tags in the collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ getById(id)](./getById/#number) | Returns the structured document tag by identifier. |
|[ getByTag(tag)](./getByTag/#string) | Returns the first structured document tag encountered in the collection with the specified tag. |
|[ getByTitle(title)](./getByTitle/#string) | Returns the first structured document tag encountered in the collection with the specified title. |
|[ remove(id)](./remove/#number) | Removes the structured document tag with the specified identifier. |
|[ removeAt(index)](./removeAt/#number) | Removes a structured document tag at the specified index. |

### Examples

Shows how to get structured document tag.

```js
let doc = new aw.Document(base.myDir + "Structured document tags by id.docx");

// Get the structured document tag by Id.
let sdt = doc.range.structuredDocumentTags.getById(1160505028);
console.log(sdt.isMultiSection);
console.log(sdt.title);

// Get the structured document tag or ranged tag by Title.
sdt = doc.range.structuredDocumentTags.getByTitle("Alias4");
console.log(sdt.id);
```

### See Also

* module [Aspose.Words.Markup](../)

