---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words для .NET
description: Легко очищайте верхние и нижние колонтитулы разделов с помощью метода ClearHeadersFooters. Оптимизируйте макет документа для придания ему изысканного вида!
type: docs
weight: 120
url: /ru/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Очищает верхние и нижние колонтитулы этого раздела.

```csharp
public void ClearHeadersFooters()
```

## Примечания

Текст всех верхних и нижних колонтитулов очищается, но[`HeaderFooter`](../../headerfooter/) Сами объекты не удаляются.

Это сделает верхние и нижние колонтитулы этого раздела связанными с верхними и нижними колонтитулами предыдущего раздела.

## Примеры

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

// Очистить все верхние и нижние колонтитулы в этом разделе от всего их содержимого.
// Сами верхние и нижние колонтитулы по-прежнему будут присутствовать, но отображать их будет нечего.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Очищает верхние и нижние колонтитулы этого раздела.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| preserveWatermarks | Boolean | Верно, если водяные знаки не будут удалены. |

## Примечания

Текст всех верхних и нижних колонтитулов очищается, но[`HeaderFooter`](../../headerfooter/) Сами объекты не удаляются.

Это сделает верхние и нижние колонтитулы этого раздела связанными с верхними и нижними колонтитулами предыдущего раздела.

## Примеры

Показывает, как очистить содержимое верхнего и нижнего колонтитула с водяным знаком или без него.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Добавить простой текстовый водяной знак.
doc.Watermark.SetText("Aspose Watermark");

// Убедитесь, что верхние и нижние колонтитулы содержат контент.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Удаляет все содержимое верхнего и нижнего колонтитула, кроме водяных знаков.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Удаляет все содержимое верхнего и нижнего колонтитула, включая водяные знаки.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
