---
title: CustomXmlPart.DataChecksum
second_title: Aspose.Words per .NET API Reference
description: CustomXmlPart proprietà. Specifica un checksum del controllo di ridondanza ciclico CRC diData contenuto.
type: docs
weight: 30
url: /it/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Specifica un checksum del controllo di ridondanza ciclico (CRC) di[`Data`](../data/) contenuto.

```csharp
public long DataChecksum { get; }
```

### Esempi

Mostra come viene calcolato il checksum in un runtime.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Il checksum è di sola lettura e calcolato utilizzando i dati della corrispondente parte di dati XML personalizzata.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Abbiamo modificato la XmlPart del tag e il checksum è stato aggiornato in fase di runtime.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Guarda anche

* class [CustomXmlPart](../)
* spazio dei nomi [Aspose.Words.Markup](../../customxmlpart/)
* assemblea [Aspose.Words](../../../)


