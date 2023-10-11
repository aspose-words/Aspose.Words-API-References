---
title: Paragraph.IsDeleteRevision
second_title: Справочник по API Aspose.Words для .NET
description: Paragraph свойство. Возвращает true если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
type: docs
weight: 40
url: /ru/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsDeleteRevision { get; }
```

### Примеры

Показывает, как работать с абзацами исправлений.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Вышеуказанные абзацы не являются изменениями.
// Абзацы, которые мы добавляем после запуска отслеживания версий, будут регистрироваться как «Вставить» версии.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Абзацы, которые мы удаляем после запуска отслеживания версий, будут регистрироваться как «Удалить» версии.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Такие абзацы останутся до тех пор, пока мы не примем или не отклоним удаление ревизии.
// Принятие изменения приведет к удалению абзаца навсегда,
// и отклонение ревизии оставит ее в документе, как если бы мы ее никогда не удаляли.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Принимаем редакцию и затем проверяем, что абзаца больше нет.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)


