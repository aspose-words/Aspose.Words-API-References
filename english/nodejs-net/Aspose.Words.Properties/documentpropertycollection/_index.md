---
title: DocumentPropertyCollection class
linktitle: DocumentPropertyCollection class
articleTitle: DocumentPropertyCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Properties.DocumentPropertyCollection class. Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections"
type: docs
weight: 40
url: /nodejs-net/aspose.words.properties/documentpropertycollection/
---

## DocumentPropertyCollection class

Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/nodejs-net/work-with-document-properties/) documentation article.




### Remarks

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets number of items in the collection. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all properties from the collection. |
|[ contains(name)](./contains/#string) | Returns ``true`` if a property with the specified name exists in the collection. |
|[ indexOf(name)](./indexOf/#string) | Gets the index of a property by name. |
|[ remove(name)](./remove/#string) | Removes a property with the specified name from the collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a property at the specified index. |

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

* module [Aspose.Words.Properties](../)
* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)

