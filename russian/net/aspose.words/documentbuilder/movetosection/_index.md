---
title: DocumentBuilder.MoveToSection
linktitle: MoveToSection
articleTitle: MoveToSection
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentBuilder MoveToSection, который позволяет легко перейти к началу любого раздела текста и повысить эффективность редактирования документа.
type: docs
weight: 610
url: /ru/net/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder.MoveToSection method

Перемещает курсор в начало тела в указанном разделе.

```csharp
public void MoveToSection(int sectionIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionIndex | Int32 | Индекс раздела, к которому необходимо перейти. |

## Примечания

Когда*sectionIndex*больше или равно 0, он указывает индекс from начала документа, где 0 — первый раздел. Когда*sectionIndex* меньше 0, , то указан индекс с конца документа, где -1 соответствует последнему разделу.

Курсор перемещается на первый абзац в[`Body`](../../body/) указанного раздела.

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

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
