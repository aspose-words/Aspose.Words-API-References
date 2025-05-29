---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ViewOptions DoNotDisplayPageBoundaries улучшает ваш макет, удаляя верхнее поле и обеспечивая более чистый и профессиональный вид.
type: docs
weight: 20
url: /ru/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Отключает отображение пространства между верхом текста и верхним краем страницы.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Примеры

Показывает, как скрыть вертикальные пробелы и верхние/нижние колонтитулы в параметрах просмотра.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте контент, охватывающий 3 страницы.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Вставьте верхний и нижний колонтитулы.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Этот документ содержит небольшой объем информации, занимающий несколько полных страниц.
// Установите флаг "DoNotDisplayPageBoundaries" на "true", чтобы старые версии Microsoft Word пропускали заголовки,
// нижние колонтитулы и большая часть вертикального пустого пространства при отображении нашего документа.
// Установите флаг "DoNotDisplayPageBoundaries" на "false", чтобы получить более старые версии Microsoft Word
// для нормального отображения нашего документа.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Смотрите также

* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
