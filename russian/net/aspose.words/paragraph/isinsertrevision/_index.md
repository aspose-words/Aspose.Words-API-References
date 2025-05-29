---
title: Paragraph.IsInsertRevision
linktitle: IsInsertRevision
articleTitle: IsInsertRevision
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Paragraph IsInsertRevision в Word. Узнайте, как оно определяет вставленный текст во время отслеживания изменений для эффективного управления документами.
type: docs
weight: 110
url: /ru/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsInsertRevision { get; }
```

## Примеры

Показывает, как работать с абзацами пересмотра.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Вышеприведенные абзацы не являются изменениями.
// Абзацы, которые мы добавляем после начала отслеживания изменений, будут зарегистрированы как «Вставленные» изменения.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Абзацы, которые мы удаляем после начала отслеживания изменений, будут зарегистрированы как «Удаленные» изменения.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Такие абзацы останутся до тех пор, пока мы не примем или не отклоним удаление исправлений.
// Принятие изменения удалит абзац навсегда,
// и отклонение исправления оставит его в документе, как будто мы его никогда не удаляли.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Примите изменение, а затем убедитесь, что абзац удален.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
