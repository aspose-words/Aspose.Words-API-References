---
title: HeaderFooter.HeaderFooterType
second_title: Справочник по API Aspose.Words для .NET
description: HeaderFooter свойство. Получает тип этого верхнего/нижнего колонтитула.
type: docs
weight: 20
url: /ru/net/aspose.words/headerfooter/headerfootertype/
---
## HeaderFooter.HeaderFooterType property

Получает тип этого верхнего/нижнего колонтитула.

```csharp
public HeaderFooterType HeaderFooterType { get; }
```

### Примеры

Показывает, как создать верхний и нижний колонтитулы.

```csharp
Document doc = new Document();

// Создаем заголовок и добавляем к нему абзац. Текст в этом абзаце
// появится в верхней части каждой страницы этого раздела над основным текстом.
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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* пространство имен [Aspose.Words](../../headerfooter/)
* сборка [Aspose.Words](../../../)


