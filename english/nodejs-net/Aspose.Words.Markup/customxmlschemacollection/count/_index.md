---
title: CustomXmlSchemaCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "CustomXmlSchemaCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Markup/customxmlschemacollection/count/
---

## CustomXmlSchemaCollection.count property

Gets the number of elements contained in the collection.


```js
get count(): number
```

### Examples

Shows how to work with an XML schema collection.

```js
let doc = new aw.Document();

let xmlPartId = `{${Guid.newGuid().toString()}}`;
let xmlPartContent = "<root><text>Hello, World!</text></root>";
let xmlPart = doc.customXmlParts.add(xmlPartId, xmlPartContent);

// Add an XML schema association.
xmlPart.schemas.add("http://www.w3.org/2001/XMLSchema");

// Clone the custom XML part's XML schema association collection,
// and then add a couple of new schemas to the clone.
let schemas = xmlPart.schemas.clone();
schemas.add("http://www.w3.org/2001/XMLSchema-instance");
schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType");

expect(schemas.count).toEqual(3);
expect(schemas.indexOf("http://schemas.microsoft.com/office/2006/metadata/contentType")).toEqual(2);

// Enumerate the schemas and print each element.
for (let schema of schemas) {
  console.log(schema);
}

// Below are three ways of removing schemas from the collection.
// 1 -  Remove a schema by index:
schemas.removeAt(2);

// 2 -  Remove a schema by value:
schemas.remove("http://www.w3.org/2001/XMLSchema");

// 3 -  Use the "Clear" method to empty the collection at once.
schemas.clear();

expect(schemas.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [CustomXmlSchemaCollection](../)

