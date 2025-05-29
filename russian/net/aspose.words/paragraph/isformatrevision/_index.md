---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IsFormatRevision в Microsoft Word отслеживает изменения форматирования, обеспечивая точное редактирование документов и улучшенную совместную работу.
type: docs
weight: 90
url: /ru/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Возвращает значение true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.

```csharp
public bool IsFormatRevision { get; }
```

## Примеры

Показывает, как проверить, является ли абзац изменением формата.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Этот абзац представляет собой изменение «Формата», которое происходит, когда мы меняем форматирование существующего текста
// при отслеживании изменений в Microsoft Word через «Рецензирование» -> «Отслеживать изменения».
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
