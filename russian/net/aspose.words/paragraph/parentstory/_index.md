---
title: Paragraph.ParentStory
linktitle: ParentStory
articleTitle: ParentStory
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Paragraph ParentStory, чтобы легко получать доступ к историям на уровне родительского раздела, улучшая структуру документа с помощью параметров Body или HeaderFooter.
type: docs
weight: 210
url: /ru/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Извлекает историю уровня родительского раздела, которая может быть[`Body`](../../body/) или[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

## Примеры

Показывает, как создать верхний и нижний колонтитул.

```csharp
Document doc = new Document();

// Создаем заголовок и добавляем к нему абзац. Текст в этом абзаце
// будет отображаться в верхней части каждой страницы этого раздела, над основным текстом.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Создаем нижний колонтитул и добавляем к нему абзац. Текст в этом абзаце
// будет отображаться внизу каждой страницы этого раздела, под основным текстом.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Смотрите также

* class [Story](../../story/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
