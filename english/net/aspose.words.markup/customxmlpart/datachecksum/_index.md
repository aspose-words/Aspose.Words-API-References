---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words for .NET
description: Discover the CustomXmlPart DataChecksum property, ensuring data integrity with a reliable CRC checksum for your XML content. Enhance your data's reliability!
type: docs
weight: 30
url: /net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Specifies a cyclic redundancy check (CRC) checksum of the [`Data`](../data/) content.

```csharp
public long DataChecksum { get; }
```

## Examples

Shows how the checksum is calculated in a runtime.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// The checksum is read-only and computed using the data of the corresponding custom XML data part.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// We changed the XmlPart of the tag, and the checksum was updated at runtime.
Assert.That(updatedChecksum, Is.Not.EqualTo(checksum));
```

### See Also

* class [CustomXmlPart](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
