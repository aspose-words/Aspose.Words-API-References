---
title: HeaderFooter.IsHeader
second_title: Справочник по API Aspose.Words для .NET
description: HeaderFooter свойство. Верно если этоHeaderFooter объект является заголовком.
type: docs
weight: 30
url: /ru/net/aspose.words/headerfooter/isheader/
---
## HeaderFooter.IsHeader property

Верно, если это[`HeaderFooter`](../) объект является заголовком.

```csharp
public bool IsHeader { get; }
```

### Примеры

Показывает, как создать верхний и нижний колонтитулы.

```csharp
Document doc = new Document();

// Создаем заголовок и добавляем к нему абзац. Текст в этом абзаце
// появится вверху каждой страницы этого раздела, над основным текстом.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Создаем нижний колонтитул и добавляем к нему абзац. Текст в этом абзаце
// появится внизу каждой страницы этого раздела, под основным текстом.
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
* пространство имен [Aspose.Words](../../headerfooter/)
* сборка [Aspose.Words](../../../)


