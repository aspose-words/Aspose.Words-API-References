---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words per .NET
description: StructuredDocumentTag LockContents proprietà. Quando impostato suVERO  questa proprietà impedirà a un utente di modificarne il contenutoSDT  in C#.
type: docs
weight: 200
url: /it/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

Quando impostato su`VERO` , questa proprietà impedirà a un utente di modificarne il contenuto**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Esempi

Mostra come applicare restrizioni di modifica ai tag dei documenti strutturati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un tag di documento strutturato in testo semplice, che funge da casella di testo che richiede all'utente di compilarlo.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "LockContents" su "true" per impedire all'utente di modificare il contenuto di questa casella di testo.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "LockContentControl" su "true" per impedirne l'accesso all'utente
// elimina manualmente questo tag di documento strutturato in Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
