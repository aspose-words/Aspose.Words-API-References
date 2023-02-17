---
title: Class CustomXmlSchemaCollection
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Markup.CustomXmlSchemaCollection class. A collection of strings that represent XML schemas that are associated with a custom XML part in C#.
type: docs
weight: 3750
url: /net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

A collection of strings that represent XML schemas that are associated with a custom XML part.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Gets or sets the element at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(string) | Adds an item to the collection. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Removes all elements from the collection. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Makes a deep clone of this object. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(string) | Returns the zero-based index of the specified value in the collection. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(string) | Removes the specified value from the collection. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(int) | Removes a value at the specified index. |

## Remarks

You do not create instances of this class. You access the collection of XML schemas of a custom XML part via the [`Schemas`](../customxmlpart/schemas/) property.

## Examples

Shows how to work with an XML schema collection.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Add an XML schema association.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clone the custom XML part's XML schema association collection,
// and then add a couple of new schemas to the clone.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Enumerate the schemas and print each element.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Below are three ways of removing schemas from the collection.
// 1 -  Remove a schema by index:
schemas.RemoveAt(2);

// 2 -  Remove a schema by value:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 -  Use the "Clear" method to empty the collection at once.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### See Also

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
