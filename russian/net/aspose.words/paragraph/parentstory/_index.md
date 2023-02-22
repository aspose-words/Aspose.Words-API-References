---
title: Paragraph.ParentStory
second_title: Справочник по API Aspose.Words для .NET
description: Paragraph свойство. Извлекает историю на уровне родительского раздела которую можноBody или жеHeaderFooter .
type: docs
weight: 210
url: /ru/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Извлекает историю на уровне родительского раздела, которую можно[`Body`](../../body/) или же[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
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

* class [Story](../../story/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)


