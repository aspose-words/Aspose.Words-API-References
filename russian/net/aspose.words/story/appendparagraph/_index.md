---
title: Story.AppendParagraph
second_title: Справочник по API Aspose.Words для .NET
description: Story метод. Ярлык метода создающийParagraph объект с необязательным текстом и добавляет его в конец этого объекта.
type: docs
weight: 60
url: /ru/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

Ярлык метода, создающий[`Paragraph`](../../paragraph/) объект с необязательным текстом и добавляет его в конец этого объекта.

```csharp
public Paragraph AppendParagraph(string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | String | Текст абзаца. Возможно`нулевой` или пустая строка. |

### Возвращаемое значение

Вновь созданный и добавленный абзац.

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* пространство имен [Aspose.Words](../../story/)
* сборка [Aspose.Words](../../../)


