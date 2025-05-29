---
title: PageSetup.OddAndEvenPagesHeaderFooter
linktitle: OddAndEvenPagesHeaderFooter
articleTitle: OddAndEvenPagesHeaderFooter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup OddAndEvenPagesHeaderFooter для создания уникальных верхних и нижних колонтитулов на четных и нечетных страницах, что улучшит представление вашего документа.
type: docs
weight: 280
url: /ru/net/aspose.words/pagesetup/oddandevenpagesheaderfooter/
---
## PageSetup.OddAndEvenPagesHeaderFooter property

Истинно, если документ имеет разные верхние и нижние колонтитулы для четных и нечетных страниц.

```csharp
public bool OddAndEvenPagesHeaderFooter { get; set; }
```

## Примечания

Обратите внимание, что изменение этого свойства влияет на все разделы документа.

## Примеры

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создаем заголовки, затем добавляем в документ три страницы для отображения каждого типа заголовков.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Показывает, как включить или отключить верхние/нижние колонтитулы страниц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа верхних/нижних колонтитулов.
// 1 — «Основной» верхний/нижний колонтитул, который отображается на каждой странице раздела.
// Мы можем переопределить основной верхний/нижний колонтитул первой и четной страницы.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

// 2 - «Четный» верхний/нижний колонтитул, который отображается на каждой четной странице этого раздела.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Writeln("Even page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterEven);
builder.Writeln("Even page footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Каждый раздел имеет объект "PageSetup", который определяет свойства, связанные с внешним видом страницы
// такие как ориентация, размер и границы.
// Установите свойство "OddAndEvenPagesHeaderFooter" в значение "true"
// для отображения верхнего/нижнего колонтитула четных страниц.
// Установите свойство "OddAndEvenPagesHeaderFooter" в значение "false"
// для отображения основного верхнего/нижнего колонтитула на четных страницах.
builder.PageSetup.OddAndEvenPagesHeaderFooter = oddAndEvenPagesHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
