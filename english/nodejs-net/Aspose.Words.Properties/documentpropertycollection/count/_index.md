---
title: DocumentPropertyCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "DocumentPropertyCollection.count property. Gets number of items in the collection."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Properties/documentpropertycollection/count/
---

## DocumentPropertyCollection.count property

Gets number of items in the collection.


```js
get count(): number
```

### Examples

Shows how to work with custom document properties.

```js
let doc = new aw.Document(base.myDir + "Properties.docx");

// Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
// The document has a fixed list of built-in properties. The user creates all of the custom properties. 
expect(doc.customDocumentProperties.at("CustomProperty").toString()).toEqual("Value of custom document property");

doc.customDocumentProperties.add("CustomProperty2", "Value of custom document property #2");

/*console.log("Custom Properties:");
for (let customDocumentProperty of doc.customDocumentProperties)
{
  console.log(customDocumentProperty.name);
  console.log(`\tType:\t${customDocumentProperty.type}`);
  console.log(`\tValue:\t\"${customDocumentProperty.toString()}\"`);
}*/
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [DocumentPropertyCollection](../)

