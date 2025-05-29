---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words per .NET
description: Scopri la proprietà Comment DateTimeUtc, che recupera la data e l'ora UTC esatte dei tuoi commenti per un monitoraggio e una gestione accurati.
type: docs
weight: 50
url: /it/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Ottiene la data e l'ora UTC in cui è stato fatto il commento.

```csharp
public DateTime DateTimeUtc { get; }
```

## Osservazioni

Il valore predefinito è MinValue

## Esempi

Mostra come ottenere la data e l'ora UTC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

DateTime dateTime = DateTime.Now;
Comment comment = new Comment(doc, "John Doe", "J.D.", dateTime);
comment.SetText("My comment.");

builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.UtcDateTime.docx");
doc = new Document(ArtifactsDir + "Comment.UtcDateTime.docx");

comment = (Comment)doc.GetChild(NodeType.Comment, 0, true);
// DateTimeUtc restituisce i dati senza millisecondi.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Guarda anche

* class [Comment](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
