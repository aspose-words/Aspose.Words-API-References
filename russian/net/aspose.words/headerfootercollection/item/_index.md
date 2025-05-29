---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Доступ к HeaderFooters без усилий с помощью свойства Item. Извлекайте определенные верхние или нижние колонтитулы по индексу для упрощенного управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Извлекает[`HeaderFooter`](../../headerfooter/) по данному индексу.

```csharp
public HeaderFooter this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Указатель коллекции. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и т. д.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается пустая ссылка.

## Примеры

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
// верхний и нижний колонтитулы будут отображаться только на страницах раздела, который их содержит.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Мы можем связать верхние/нижние колонтитулы раздела с верхними/нижними колонтитулами предыдущего раздела
// чтобы разрешить разделу ссылки отображать верхние/нижние колонтитулы связанного раздела.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Каждый раздел все равно будет иметь свои собственные объекты заголовка/подвала. Когда мы связываем разделы,
// раздел ссылки будет отображать верхние/нижние колонтитулы связанного раздела, сохраняя свои собственные.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Свяжите верхние/нижние колонтитулы третьего раздела с верхними/нижними колонтитулами второго раздела.
// Второй раздел уже ссылается на верхний/нижний колонтитулы первого раздела,
// поэтому ссылка на второй раздел создаст цепочку ссылок.
// Первый, второй, а теперь и третий разделы будут отображать заголовки первого раздела.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// Мы можем отменить привязку верхних/нижних колонтитулов предыдущего раздела, передав «false» при вызове метода LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// С помощью этого метода мы также можем выбрать только определенный тип верхнего/нижнего колонтитула для ссылки.
// Третий раздел теперь будет иметь тот же нижний колонтитул, что и второй и первый разделы, но не верхний колонтитул.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// Верхний/нижний колонтитулы первого раздела не могут быть связаны ни с чем, поскольку предыдущего раздела нет.
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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Извлекает[`HeaderFooter`](../../headerfooter/) указанного типа.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Параметр | Описание |
| --- | --- |
| headerFooterType | А[`HeaderFooterType`](../../headerfootertype/) value , который указывает тип извлекаемого верхнего/нижнего колонтитула. |

## Примечания

Возврат`нулевой`если верхний/нижний колонтитул указанного типа не найден.

## Примеры

Показывает, как заменить текст в нижнем колонтитуле документа.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Показывает, как удалить все нижние колонтитулы из документа.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Проходим по каждому разделу и удаляем нижние колонтитулы всех видов.
foreach (Section section in doc.OfType<Section>())
{
    // Существует три типа нижних и верхних колонтитулов.
    // 1 — «Первый» верхний/нижний колонтитул, который отображается только на первой странице раздела.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 — «Основной» верхний/нижний колонтитул, который отображается на нечетных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - «Четный» верхний/нижний колонтитул, который отображается на четных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Смотрите также

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
