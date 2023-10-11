---
title: HeaderFooterCollection.LinkToPrevious
second_title: Справочник по API Aspose.Words для .NET
description: HeaderFooterCollection метод. Связывает или отключает все верхние и нижние колонтитулы с соответствующими верхними и нижними колонтитулами в предыдущем разделе.
type: docs
weight: 20
url: /ru/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(bool) {#linktoprevious_1}

Связывает или отключает все верхние и нижние колонтитулы с соответствующими верхними и нижними колонтитулами в предыдущем разделе.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `истинный` чтобы связать верхние и нижние колонтитулы с предыдущим разделом; `ЛОЖЬ` чтобы разъединить их. |

### Примечания

Если какие-либо верхние или нижние колонтитулы не существуют, они создаются автоматически.

### Примеры

Показывает, как связать верхние и нижние колонтитулы между разделами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Переходим к первому разделу и создаем верхний и нижний колонтитулы. По умолчанию,
// верхний и нижний колонтитулы будут отображаться только на страницах того раздела, который их содержит.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Мы можем связать верхние/нижние колонтитулы раздела с верхними/нижними колонтитулами предыдущего раздела
// чтобы позволить разделу ссылки отображать верхние и нижние колонтитулы связанного раздела.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Каждый раздел по-прежнему будет иметь свои собственные объекты верхнего и нижнего колонтитула. Когда мы связываем разделы,
// раздел ссылки будет отображать верхний/нижний колонтитул связанного раздела, сохраняя при этом свои собственные.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Связываем верхние/нижние колонтитулы третьего раздела с верхними/нижними колонтитулами второго раздела.
// Второй раздел уже ссылается на верхний/нижний колонтитул первого раздела,
// поэтому ссылка на второй раздел создаст цепочку ссылок.
// Первый, второй и теперь третий разделы будут отображать заголовки первого раздела.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Мы можем отменить связь верхнего и нижнего колонтитулов предыдущего раздела, передав «false» при вызове метода LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Мы также можем выбрать только определенный тип верхнего/нижнего колонтитула для ссылки, используя этот метод.
// Третий раздел теперь будет иметь тот же нижний колонтитул, что и второй и первый разделы, но не заголовок.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Верхние/нижние колонтитулы первого раздела не могут связать себя ни с чем, поскольку предыдущего раздела нет.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Все верхние/нижние колонтитулы второго раздела связаны с верхними/нижними колонтитулами первого раздела.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// В третьем разделе только нижний колонтитул связан с нижним колонтитулом первого раздела через второй раздел.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Смотрите также

* class [HeaderFooterCollection](../)
* пространство имен [Aspose.Words](../../headerfootercollection/)
* сборка [Aspose.Words](../../../)

---

## LinkToPrevious(HeaderFooterType, bool) {#linktoprevious}

Связывает или отменяет связь указанного верхнего или нижнего колонтитула с соответствующим заголовком или нижним колонтитулом в предыдущем разделе.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | А[`HeaderFooterType`](../../headerfootertype/) value , указывающее верхний или нижний колонтитул для связывания/отсоединения. |
| isLinkToPrevious | Boolean | `истинный`чтобы связать верхний или нижний колонтитул с предыдущим разделом; `ЛОЖЬ` чтобы отменить связь. |

### Примечания

Если верхний или нижний колонтитул указанного типа не существует, создает его автоматически.

### Примеры

Показывает, как связать верхние и нижние колонтитулы между разделами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// Переходим к первому разделу и создаем верхний и нижний колонтитулы. По умолчанию,
// верхний и нижний колонтитулы будут отображаться только на страницах того раздела, который их содержит.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Мы можем связать верхние/нижние колонтитулы раздела с верхними/нижними колонтитулами предыдущего раздела
// чтобы позволить разделу ссылки отображать верхние и нижние колонтитулы связанного раздела.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Каждый раздел по-прежнему будет иметь свои собственные объекты верхнего и нижнего колонтитула. Когда мы связываем разделы,
// раздел ссылки будет отображать верхний/нижний колонтитул связанного раздела, сохраняя при этом свои собственные.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Связываем верхние/нижние колонтитулы третьего раздела с верхними/нижними колонтитулами второго раздела.
// Второй раздел уже ссылается на верхний/нижний колонтитул первого раздела,
// поэтому ссылка на второй раздел создаст цепочку ссылок.
// Первый, второй и теперь третий разделы будут отображать заголовки первого раздела.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Мы можем отменить связь верхнего и нижнего колонтитулов предыдущего раздела, передав «false» при вызове метода LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Мы также можем выбрать только определенный тип верхнего/нижнего колонтитула для ссылки, используя этот метод.
// Третий раздел теперь будет иметь тот же нижний колонтитул, что и второй и первый разделы, но не заголовок.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Верхние/нижние колонтитулы первого раздела не могут связать себя ни с чем, поскольку предыдущего раздела нет.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// Все верхние/нижние колонтитулы второго раздела связаны с верхними/нижними колонтитулами первого раздела.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// В третьем разделе только нижний колонтитул связан с нижним колонтитулом первого раздела через второй раздел.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Смотрите также

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* пространство имен [Aspose.Words](../../headerfootercollection/)
* сборка [Aspose.Words](../../../)


