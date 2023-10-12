---
title: DocumentBuilder.CurrentStructuredDocumentTag
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. Ruft das strukturierte DokumentTag ab das derzeit hier ausgewählt istDocumentBuilder .
type: docs
weight: 80
url: /de/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Ruft das strukturierte Dokument-Tag ab, das derzeit hier ausgewählt ist[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

### Beispiele

Zeigt, wie der Cursor von DocumentBuilder innerhalb eines strukturierten Dokument-Tags bewegt wird.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 – Nach Index zum ersten Zeichen des strukturierten Dokument-Tags wechseln.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 – Zum ersten Zeichen des strukturierten Dokuments wechseln, Tag für Objekt.
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
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


