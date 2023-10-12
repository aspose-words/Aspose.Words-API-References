---
title: Section.ClearHeadersFooters
second_title: Справочник по API Aspose.Words для .NET
description: Section метод. Очищает верхние и нижние колонтитулы этого раздела.
type: docs
weight: 120
url: /ru/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

Очищает верхние и нижние колонтитулы этого раздела.

```csharp
public void ClearHeadersFooters()
```

### Примечания

Текст всех верхних и нижних колонтитулов очищается, но[`HeaderFooter`](../../headerfooter/) сами объекты не удаляются.

Это сделает верхние и нижние колонтитулы этого раздела связанными с верхними и нижними колонтитулами предыдущего раздела.

### Примеры

Показывает, как очистить содержимое всех верхних и нижних колонтитулов в разделе.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Очищаем все верхние и нижние колонтитулы в этом разделе от всего их содержимого.
// Сами верхние и нижние колонтитулы по-прежнему будут присутствовать, но отображать им будет нечего.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


