---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsAtEndOfStructuredDocumentTag-Eigenschaft von DocumentBuilder – prüfen Sie, ob Ihr Cursor am Ende eines strukturierten Dokument-Tags positioniert ist, um eine effiziente Bearbeitung zu ermöglichen!
type: docs
weight: 120
url: /de/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Rückgaben**WAHR** wenn sich der Cursor am Ende eines strukturierten Dokument-Tags befindet.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
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

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
