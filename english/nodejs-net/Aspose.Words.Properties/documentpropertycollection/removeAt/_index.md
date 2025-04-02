---
title: DocumentPropertyCollection.removeAt method
linktitle: removeAt method
articleTitle: removeAt method
second_title: Aspose.Words for NodeJs
description: "DocumentPropertyCollection.removeAt method. Removes a property at the specified index."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Properties/documentpropertycollection/removeAt/
---

## removeAt(index) {#number}

Removes a property at the specified index.


```js
removeAt(index: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero based index. |

### Examples

Shows how to work with a document's custom properties.

```js
let doc = new aw.Document();
let properties = doc.customDocumentProperties;

expect(properties.count).toEqual(0);

// Custom document properties are key-value pairs that we can add to the document.
properties.add("Authorized", true);
properties.add("Authorized By", "John Doe");
properties.add("Authorized Date", Date.now());
properties.add("Authorized Revision", doc.builtInDocumentProperties.revisionNumber);
properties.add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
expect(properties.indexOf("Authorized Amount")).toEqual(1);
expect(properties.count).toEqual(5);

// Print every custom property in the document.
/*for (let p of properties) {
    console.log(`Name: \"${p.name}\"\n\tType: \"${p.type}\"\n\tValue: \"${p.toString()}\"`);
}*/

// Display the value of a custom property using a DOCPROPERTY field.
let builder = new aw.DocumentBuilder(doc);
let field = builder.insertField(" DOCPROPERTY \"Authorized By\"").asFieldDocProperty();
field.update();

expect(field.result).toEqual("John Doe");

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(base.artifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.removeAt(1);

expect(properties.contains("Authorized Amount")).toEqual(false);
expect(properties.count).toEqual(4);

// 2 -  Remove by name:
properties.remove("Authorized Revision");

expect(properties.contains("Authorized Revision")).toEqual(false);
expect(properties.count).toEqual(3);

// 3 -  Empty the entire collection at once:
properties.clear();

expect(properties.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [DocumentPropertyCollection](../)

