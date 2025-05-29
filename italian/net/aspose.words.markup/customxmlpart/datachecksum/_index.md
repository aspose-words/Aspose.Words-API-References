---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words per .NET
description: Scopri la proprietà DataChecksum di CustomXmlPart, che garantisce l'integrità dei dati con un checksum CRC affidabile per i tuoi contenuti XML. Migliora l'affidabilità dei tuoi dati!
type: docs
weight: 30
url: /it/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Specifica un checksum del controllo di ridondanza ciclico (CRC) del[`Data`](../data/) contenuto.

```csharp
public long DataChecksum { get; }
```

## Esempi

Mostra come viene calcolato il checksum in fase di esecuzione.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Il checksum è di sola lettura e viene calcolato utilizzando i dati della parte di dati XML personalizzata corrispondente.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Abbiamo modificato la parte XmlPart del tag e il checksum è stato aggiornato in fase di esecuzione.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Guarda anche

* class [CustomXmlPart](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
