---
title: HeaderFooter.IsHeader
linktitle: IsHeader
articleTitle: IsHeader
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IsHeader объекта HeaderFooter — легко определите, является ли ваш объект HeaderFooter заголовком для упрощенного форматирования документа.
type: docs
weight: 30
url: /ru/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

Истина, если это[`HeaderFooter`](../) объект является заголовком.

```csharp
public bool IsHeader { get; }
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

* class [HeaderFooter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
