---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Kommentar DateTimeUtc, som hämtar exakt UTC-datum och tid för dina kommentarer för korrekt spårning och hantering.
type: docs
weight: 50
url: /sv/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Hämtar UTC-datum och -tid då kommentaren gjordes.

```csharp
public DateTime DateTimeUtc { get; }
```

## Anmärkningar

Standardvärdet är MinValue

## Exempel

Visar hur man får UTC-datum och -tid.

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
// DateTimeUtc returnerar data utan millisekunder.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Se även

* class [Comment](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
