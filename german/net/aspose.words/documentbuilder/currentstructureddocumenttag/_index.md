---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die CurrentStructuredDocumentTag-Eigenschaft in DocumentBuilder. Greifen Sie einfach auf das ausgewählte strukturierte Dokument-Tag zu und verwalten Sie Ihre Dokumente effizient.
type: docs
weight: 80
url: /de/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Ruft das strukturierte Dokument-Tag ab, das derzeit in diesem[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Wechseln Sie nach Index zum ersten Zeichen des strukturierten Dokument-Tags.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Wechseln Sie zum ersten Zeichen des strukturierten Dokument-Tags nach Objekt.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 – Zum Ende des zweiten strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Aktuell ausgewähltes strukturiertes Dokument-Tag abrufen.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
