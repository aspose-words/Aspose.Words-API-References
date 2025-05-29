---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: .NET için Aspose.Words
description: Yorumlarınızın doğru takibi ve yönetimi için tam UTC tarih ve saatini alan Comment DateTimeUtc özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Yorumun yapıldığı UTC tarih ve saatini alır.

```csharp
public DateTime DateTimeUtc { get; }
```

## Notlar

Varsayılan değer MinValue

## Örnekler

UTC tarih ve saatinin nasıl alınacağını gösterir.

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
// DateTimeUtc milisaniyeler olmadan veri döndürür.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Ayrıca bakınız

* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
