---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words for .NET
description: Discover the XmlMapping PrefixMappings property for seamless XML namespace prefix mapping and efficient XPath evaluation. Enhance your XML processing today!
type: docs
weight: 30
url: /net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

Returns XML namespace prefix mappings to evaluate the [`XPath`](../xpath/).

```csharp
public string PrefixMappings { get; }
```

## Remarks

Specifies the set of prefix mappings, which shall be used to interpret the XPath expression when the XPath expression is evaluated against the custom XML data parts in the document.

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

* class [XmlMapping](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
