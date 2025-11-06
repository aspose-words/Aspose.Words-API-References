---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Markup.CustomXmlPartCollection class, your go-to solution for managing Custom XML Parts efficiently and effortlessly.
type: docs
weight: 4650
url: /net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Represents a collection of Custom XML Parts. The items are [`CustomXmlPart`](../customxmlpart/) objects.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Constructors

| Name | Description |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Gets the number of elements contained in the collection. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Gets or sets an item at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Adds an item to the collection. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Creates a new XML part with the specified XML and adds it to the collection. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Removes all elements from the collection. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Makes a deep copy of this collection and its items. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Finds and returns a custom XML part by its identifier. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Removes an item at the specified index. |

## Remarks

You do not normally need to create instances of this class. You can access custom XML data stored in a document via the [`CustomXmlParts`](../../aspose.words/document/customxmlparts/) property.

## Examples

Shows how to create a structured document tag with custom XML data.

```csharp
Document doc = new Document();

// Construct an XML part that contains data and add it to the document's collection.
// If we enable the "Developer" tab in Microsoft Word,
// we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.That(xmlPart.Data, Is.EqualTo(Encoding.ASCII.GetBytes(xmlPartContent)));
Assert.That(xmlPart.Id, Is.EqualTo(xmlPartId));

// Below are two ways to refer to XML parts.
// 1 -  By an index in the custom XML part collection:
Assert.That(doc.CustomXmlParts[0], Is.EqualTo(xmlPart));

// 2 -  By GUID:
Assert.That(doc.CustomXmlParts.GetById(xmlPartId), Is.EqualTo(xmlPart));

// Add an XML schema association.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Clone a part, and then insert it into the collection.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.That(doc.CustomXmlParts.Count, Is.EqualTo(2));

// Iterate through the collection and print the contents of each part.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Use the "RemoveAt" method to remove the cloned part by index.
doc.CustomXmlParts.RemoveAt(1);

Assert.That(doc.CustomXmlParts.Count, Is.EqualTo(1));

// Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Create a structured document tag that will display our part's contents and insert it into the document body.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### See Also

* class [CustomXmlPart](../customxmlpart/)
* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
