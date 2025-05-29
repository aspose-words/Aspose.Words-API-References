---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words per .NET
description: Scopri la proprietà CurrentStructuredDocumentTag in DocumentBuilder. Accedi facilmente al tag del documento strutturato selezionato per una gestione efficiente dei documenti.
type: docs
weight: 80
url: /it/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Ottiene il tag del documento strutturato attualmente selezionato in questo[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Esempi

Mostra come spostare il cursore di DocumentBuilder all'interno di un tag di documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono diversi modi per spostare il cursore:
// 1 - Passa al primo carattere del tag del documento strutturato tramite l'indice.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Passa al primo carattere del tag del documento strutturato tramite oggetto.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - Spostarsi alla fine del secondo tag del documento strutturato.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Ottieni il tag del documento strutturato attualmente selezionato.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
