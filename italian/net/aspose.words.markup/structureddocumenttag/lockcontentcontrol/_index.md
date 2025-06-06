---
title: StructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words per .NET
description: Scopri come la proprietà LockContentControl di StructuredDocumentTag migliora la sicurezza dei documenti impedendo agli utenti di eliminare contenuti essenziali. Scopri di più!
type: docs
weight: 190
url: /it/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

Quando impostato su`VERO` , questa proprietà impedirà a un utente di eliminare questo**SDT** .

```csharp
public bool LockContentControl { get; set; }
```

## Esempi

Mostra come applicare restrizioni di modifica ai tag dei documenti strutturati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un tag di documento strutturato in testo normale, che funge da casella di testo che richiede all'utente di compilarlo.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Impostare la proprietà "LockContents" su "true" per impedire all'utente di modificare il contenuto di questa casella di testo.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Imposta la proprietà "LockContentControl" su "true" per impedire all'utente di
// eliminare manualmente questo tag di documento strutturato in Microsoft Word.
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
