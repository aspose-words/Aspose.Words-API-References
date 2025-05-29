---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words für .NET
description: Entdecken Sie die CustomXmlPart DataChecksum-Eigenschaft, die die Datenintegrität mit einer zuverlässigen CRC-Prüfsumme für Ihre XML-Inhalte sicherstellt. Steigern Sie die Zuverlässigkeit Ihrer Daten!
type: docs
weight: 30
url: /de/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Gibt eine CRC-Prüfsumme (Cyclic Redundancy Check) der[`Data`](../data/) Inhalt.

```csharp
public long DataChecksum { get; }
```

## Beispiele

Zeigt, wie die Prüfsumme in einer Laufzeit berechnet wird.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Die Prüfsumme ist schreibgeschützt und wird anhand der Daten des entsprechenden benutzerdefinierten XML-Datenteils berechnet.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Wir haben den XmlPart des Tags geändert und die Prüfsumme wurde zur Laufzeit aktualisiert.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Siehe auch

* class [CustomXmlPart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
