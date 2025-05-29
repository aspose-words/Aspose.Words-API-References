---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words für .NET
description: Entdecken Sie die SdtType-Eigenschaft von StructuredDocumentTag, um Tag-Typen einfach zu identifizieren und so Ihre Dokumentenverwaltung und -organisation zu verbessern.
type: docs
weight: 250
url: /de/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Ruft den Typ dieses**Strukturiertes Dokument-Tag** .

```csharp
public SdtType SdtType { get; }
```

## Beispiele

Zeigt, wie der Typ eines strukturierten Dokument-Tags abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Siehe auch

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
