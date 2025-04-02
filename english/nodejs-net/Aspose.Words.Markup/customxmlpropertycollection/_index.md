---
title: CustomXmlPropertyCollection class
linktitle: CustomXmlPropertyCollection class
articleTitle: CustomXmlPropertyCollection class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.CustomXmlPropertyCollection class. Represents a collection of custom XML attributes or smart tag properties"
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Markup/customxmlpropertycollection/
---

## CustomXmlPropertyCollection class

Represents a collection of custom XML attributes or smart tag properties.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

Items are [CustomXmlProperty](../customxmlproperty/) objects.




### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |
| [this[]](./this[]/) |  |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(property)](./add/#customxmlproperty) | Adds a property to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(name)](./contains/#string) | Determines whether the collection contains a property with the given name. |
|[ indexOfKey(name)](./indexOfKey/#string) | Returns the zero-based index of the specified property in the collection. |
|[ remove(name)](./remove/#string) | Removes a property with the specified name from the collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a property at the specified index. |

### Examples

Shows how to work with smart tag properties to get in depth information about smart tags.

```js
let doc = new aw.Document(base.myDir + "Smart tags.doc");

// A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
// such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
// In Word 2003, we can enable smart tags via "Tools" -> "AutoCorrect options..." -> "SmartTags".
// In our input document, there are three objects that Microsoft Word registered as smart tags.
// Smart tags may be nested, so this collection contains more.
let smartTags = doc.getChildNodes(aw.NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

expect(smartTags.length).toEqual(8);

// The "Properties" member of a smart tag contains its metadata, which will be different for each type of smart tag.
// The properties of a "date"-type smart tag contain its year, month, and day.
let properties = smartTags.at(7).properties;

expect(properties.count).toEqual(4);

using (IEnumerator<CustomXmlProperty> enumerator = properties.getEnumerator())
{
  while (enumerator.moveNext())
  {
    console.log(`Property name: ${enumerator.current.name}, value: ${enumerator.current.value}`);
    expect(enumerator.current.uri).toEqual("");
  }
}

// We can also access the properties in various ways, such as a key-value pair.
expect(properties.contains("Day")).toEqual(true);
expect(properties.at("Day").value).toEqual("22");
expect(properties.at(2).value).toEqual("2003");
expect(properties.indexOfKey("Month")).toEqual(1);

// Below are three ways of removing elements from the properties collection.
// 1 -  Remove by index:
properties.removeAt(3);

expect(properties.count).toEqual(3);

// 2 -  Remove by name:
properties.remove("Year");

expect(properties.count).toEqual(2);

// 3 -  Clear the entire collection at once:
properties.clear();

expect(properties.count).toEqual(0);
```

### See Also

* module [Aspose.Words.Markup](../)

