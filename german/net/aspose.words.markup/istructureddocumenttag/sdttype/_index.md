---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IStructuredDocumentTag SdtType“, um den Typ strukturierter Dokument-Tags für eine verbesserte Dokumentenverwaltung einfach zu identifizieren.
type: docs
weight: 120
url: /de/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

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
* interface [IStructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
