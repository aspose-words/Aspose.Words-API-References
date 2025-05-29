---
title: HeaderFooter
linktitle: HeaderFooter
articleTitle: HeaderFooter
second_title: Aspose.Words для .NET
description: Создавайте потрясающие заголовки и нижние колонтитулы без усилий с помощью нашего интуитивно понятного конструктора. Настройте внешний вид вашего веб-сайта для уникального, профессионального штриха!
type: docs
weight: 10
url: /ru/net/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter constructor

Создает новый верхний или нижний колонтитул указанного типа.

```csharp
public HeaderFooter(DocumentBase doc, HeaderFooterType headerFooterType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| headerFooterType | HeaderFooterType | А[`HeaderFooterType`](../headerfootertype/)value , указывающее тип верхнего или нижнего колонтитула. |

## Примечания

Когда[`HeaderFooter`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../node/parentnode/) является`нулевой`.

Чтобы добавить[`HeaderFooter`](../)к[`Section`](../../section/) использовать[`InsertAfter`](../../compositenode/insertafter/) ,[`InsertBefore`](../../compositenode/insertbefore/) , или[`HeadersFooters`](../../section/headersfooters/) свойство и методы[`Add`](../../nodecollection/add/) ,[`Insert`](../../nodecollection/insert/).

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

* class [DocumentBase](../../documentbase/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooter](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
