---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words für .NET
description: Entdecken Sie die DateTimeUtc-Eigenschaft „Comment“, die das genaue UTC-Datum und die UTC-Uhrzeit Ihrer Kommentare abruft, um eine genaue Verfolgung und Verwaltung zu ermöglichen.
type: docs
weight: 50
url: /de/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Ruft das UTC-Datum und die UTC-Uhrzeit ab, zu der der Kommentar erstellt wurde.

```csharp
public DateTime DateTimeUtc { get; }
```

## Bemerkungen

Der Standardwert ist MinValue

## Beispiele

Zeigt, wie man UTC-Datum und -Uhrzeit erhält.

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
// DateTimeUtc gibt Daten ohne Millisekunden zurück.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Siehe auch

* class [Comment](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
