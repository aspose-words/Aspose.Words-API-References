---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CustomXmlPart DataChecksum, som säkerställer dataintegritet med en pålitlig CRC-kontrollsumma för ditt XML-innehåll. Förbättra dina datas tillförlitlighet!
type: docs
weight: 30
url: /sv/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Anger en cyklisk redundanskontroll (CRC) för[`Data`](../data/) innehåll.

```csharp
public long DataChecksum { get; }
```

## Exempel

Visar hur kontrollsumman beräknas i en körning.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Kontrollsumman är skrivskyddad och beräknas med hjälp av data från motsvarande anpassade XML-datadel.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Vi ändrade XmlPart i taggen och kontrollsumman uppdaterades vid körning.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Se även

* class [CustomXmlPart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
