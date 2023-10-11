---
title: Enum HeaderFooterType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.HeaderFooterType перечисление. Определяет тип верхнего или нижнего колонтитула в файле Word.
type: docs
weight: 3120
url: /ru/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

Определяет тип верхнего или нижнего колонтитула в файле Word.

```csharp
public enum HeaderFooterType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| HeaderEven | `0` | Заголовок для четных страниц. |
| HeaderPrimary | `1` | Основной заголовок, также используется для страниц с нечетными номерами. |
| FooterEven | `2` | Нижний колонтитул для четных страниц. |
| FooterPrimary | `3` | Основной нижний колонтитул, также используется для страниц с нечетными номерами. |
| HeaderFirst | `4` | Заголовок первой страницы раздела. |
| FooterFirst | `5` | Нижний колонтитул первой страницы раздела. |

### Примеры

Показывает, как создавать верхние и нижние колонтитулы в документе с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Указываем, что нам нужны разные верхние и нижние колонтитулы для первой, четной и нечетной страниц.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Создайте заголовки, затем добавьте в документ три страницы для отображения каждого типа заголовка.
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


