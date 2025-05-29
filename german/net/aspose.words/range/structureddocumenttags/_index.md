---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words für .NET
description: Entdecken Sie die Range StructuredDocumentTags-Eigenschaft, die eine umfassende Sammlung strukturierter Dokument-Tags bereitstellt und so die Organisation und Funktionalität Ihres Dokuments verbessert.
type: docs
weight: 50
url: /de/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Gibt einen`StructuredDocumentTags` Sammlung, die alle strukturierten Dokument-Tags im Bereich darstellt.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## Beispiele

Zeigt, wie strukturierte Dokument-Tags entfernt werden.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
// Entfernen Sie das strukturierte Dokument-Tag anhand der ID.
structuredDocumentTags.Remove(1691867797);
// Entfernen Sie das strukturierte Dokument-Tag an Position 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Siehe auch

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
