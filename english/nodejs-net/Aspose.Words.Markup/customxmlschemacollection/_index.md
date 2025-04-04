---
title: CustomXmlSchemaCollection class
linktitle: CustomXmlSchemaCollection class
articleTitle: CustomXmlSchemaCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Markup.CustomXmlSchemaCollection class. A collection of strings that represent XML schemas that are associated with a custom XML part"
type: docs
weight: 70
url: /nodejs-net/aspose.words.markup/customxmlschemacollection/
---

## CustomXmlSchemaCollection class

A collection of strings that represent XML schemas that are associated with a custom XML part.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

You do not create instances of this class. You access the collection of XML schemas of a custom XML part
via the [CustomXmlPart.schemas](../customxmlpart/schemas/) property.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#string) | Adds an item to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ clone()](./clone/#default) | Makes a deep clone of this object. |
|[ indexOf(value)](./indexOf/#string) | Returns the zero-based index of the specified value in the collection. |
|[ remove(name)](./remove/#string) | Removes the specified value from the collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a value at the specified index. |

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

* module [Aspose.Words.Markup](../)
* class [CustomXmlPart](../customxmlpart/)
* property [CustomXmlPart.schemas](../customxmlpart/schemas/)

