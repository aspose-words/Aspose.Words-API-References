---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Comment DateTimeUtc, которое извлекает точную дату и время UTC ваших комментариев для точного отслеживания и управления.
type: docs
weight: 50
url: /ru/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

Получает дату и время UTC, когда был сделан комментарий.

```csharp
public DateTime DateTimeUtc { get; }
```

## Примечания

Значение по умолчанию: MinValue

## Примеры

Показывает, как получить дату и время в формате UTC.

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
// DateTimeUtc возвращает данные без миллисекунд.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### Смотрите также

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
