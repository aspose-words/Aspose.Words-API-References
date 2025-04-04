---
title: CustomDocumentProperties class
linktitle: CustomDocumentProperties class
articleTitle: CustomDocumentProperties class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Properties.CustomDocumentProperties class. A collection of custom document properties"
type: docs
weight: 20
url: /nodejs-net/aspose.words.properties/customdocumentproperties/
---

## CustomDocumentProperties class

A collection of custom document properties.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/nodejs-net/work-with-document-properties/) documentation article.




### Remarks

Each [DocumentProperty](../documentproperty/) object represents a custom property of a container document.




The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




**Inheritance:** [CustomDocumentProperties](./) → [DocumentPropertyCollection](../documentpropertycollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../documentpropertycollection/count/) | Gets number of items in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [this[]](../documentpropertycollection/this[]/) | <br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [this[]](../documentpropertycollection/this[]/) | <br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(name, value)](./add/#string_string) | Creates a new custom document property of the [PropertyType.String](../propertytype/#String) data type. |
|[ add(name, value)](./add/#string_number) | Creates a new custom document property of the [PropertyType.Number](../propertytype/#Number) data type. |
|[ add(name, value)](./add/#string_date) | Creates a new custom document property of the [PropertyType.DateTime](../propertytype/#DateTime) data type. |
|[ add(name, value)](./add/#string_boolean) | Creates a new custom document property of the [PropertyType.Boolean](../propertytype/#Boolean) data type. |
|[ add(name, value)](./add/#string_number) | Creates a new custom document property of the [PropertyType.Double](../propertytype/#Double) data type. |
|[ addLinkToContent(name, linkSource)](./addLinkToContent/#string_string) | Creates a new linked to content custom document property. |
|[ clear()](../documentpropertycollection/clear/#default) | Removes all properties from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ contains(name)](../documentpropertycollection/contains/#string) | Returns ``true`` if a property with the specified name exists in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ indexOf(name)](../documentpropertycollection/indexOf/#string) | Gets the index of a property by name.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove(name)](../documentpropertycollection/remove/#string) | Removes a property with the specified name from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ removeAt(index)](../documentpropertycollection/removeAt/#number) | Removes a property at the specified index.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

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

* module [Aspose.Words.Properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* class [Document](../../aspose.words/document/)
* property [Document.builtInDocumentProperties](../../aspose.words/document/builtInDocumentProperties/)
* property [Document.customDocumentProperties](../../aspose.words/document/customDocumentProperties/)

