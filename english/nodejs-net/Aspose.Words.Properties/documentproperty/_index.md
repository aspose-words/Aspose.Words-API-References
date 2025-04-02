---
title: DocumentProperty class
linktitle: DocumentProperty class
articleTitle: DocumentProperty class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Properties.DocumentProperty class. Represents a custom or built-in document property"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Properties/documentproperty/
---

## DocumentProperty class

Represents a custom or built-in document property.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/nodejs-net/work-with-document-properties/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [isLinkToContent](./isLinkToContent/) | Shows whether this property is linked to content or not. |
| [linkSource](./linkSource/) | Gets the source of a linked custom document property. |
| [name](./name/) | Returns the name of the property. |
| [type](./type/) | Gets the data type of the property. |

### Methods

| Name | Description |
| --- | --- |
|[ toBool()](./toBool/#default) | Returns the property value as bool. |
|[ toByteArray()](./toByteArray/#default) | Returns the property value as byte array. |
|[ toDateTime()](./toDateTime/#default) | Returns the property value as **DateTime** in UTC. |
|[ toDouble()](./toDouble/#default) | Returns the property value as double. |
|[ toInt()](./toInt/#default) | Returns the property value as integer. |

### Examples

Shows how to work with built-in document properties.

```js
let doc = new aw.Document(base.myDir + "Properties.docx");

// The "Document" object contains some of its metadata in its members.
//console.log(`Document filename:\n\t \"${doc.originalFileName}\"`);

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
/*console.log("Built-in Properties:");
for (let docProperty of doc.builtInDocumentProperties)
{
  console.log(docProperty.name);
  console.log(`\tType:\t${docProperty.type}`);
  console.log(`\tValue:\t\"${docProperty.toString()}\"`);
}*/
```

### See Also

* module [Aspose.Words.Properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)

