---
title: StructuredDocumentTag.LockContents
second_title: Aspose.Words per .NET API Reference
description: StructuredDocumentTag proprietà. Se impostata su true questa proprietà vieterà a un utente di modificarne il contenuto SDT .
type: docs
weight: 200
url: /it/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

Se impostata su true, questa proprietà vieterà a un utente di modificarne il contenuto **SDT** .

```csharp
public bool LockContents { get; set; }
```

### Esempi

Mostra come applicare le restrizioni di modifica ai tag di documenti strutturati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un tag di documento strutturato in testo normale, che funge da casella di testo che richiede all'utente di compilarlo.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "LockContents" su "true" per impedire all'utente di modificare il contenuto di questa casella di testo.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "LockContentControl" su "true" per impedire all'utente di farlo
// eliminando manualmente questo tag del documento strutturato in Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../structureddocumenttag/)
* assemblea [Aspose.Words](../../../)


