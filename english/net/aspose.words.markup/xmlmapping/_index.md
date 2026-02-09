---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Markup.XmlMapping class to seamlessly link structured document tags with XML elements, enhancing your document's data integration.
type: docs
weight: 4830
url: /net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document.

To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/net/working-with-content-control-sdt/) documentation article.

```csharp
public class XmlMapping
```

## Properties

| Name | Description |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Returns `true` if the parent structured document tag is successfully mapped to XML data. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Returns XML namespace prefix mappings to evaluate the [`XPath`](./xpath/). |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [`XPath`](./xpath/) expression. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |

## Methods

| Name | Description |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Deletes mapping of the parent structured document to XML data. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |

## Examples

Shows how to set XML mappings for custom XML parts.

```csharp
Document doc = new Document();

// Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.That(Encoding.UTF8.GetString(xmlPart.Data), Is.EqualTo("<root><text>Text element #1</text><text>Text element #2</text></root>"));

// Create a structured document tag that will display the contents of our CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Set a mapping for our structured document tag. This mapping will instruct
// our structured document tag to display a portion of the XML part's text contents that the XPath points to.
// In this case, it will be contents of the the second "<text>" element of the first "<root>" element: "Text element #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.That(tag.XmlMapping.IsMapped, Is.True);
Assert.That(tag.XmlMapping.CustomXmlPart, Is.EqualTo(xmlPart));
Assert.That(tag.XmlMapping.XPath, Is.EqualTo("/root[1]/text[2]"));
Assert.That(tag.XmlMapping.PrefixMappings, Is.EqualTo("xmlns:ns='http://www.w3.org/2001/XMLSchema'"));

// Add the structured document tag to the document to display the content from our custom part.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### See Also

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
