---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words для .NET
description: Управляйте макетом документа с помощью свойства PageSetup LinesPerPage. Легко настраивайте количество строк на странице для оптимальной читаемости и организации.
type: docs
weight: 240
url: /ru/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Возвращает или задает количество строк на странице в сетке документа.

```csharp
public int LinesPerPage { get; set; }
```

## Примечания

Минимальное значение свойства — 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal . Минимальный интервал между строками — 136 процентов от размера шрифта. Например, максимальное количество строк на странице формата Letter с полями в один дюйм — 39.

По умолчанию свойство имеет значение, при котором интервал строк в 1,5 раза больше размера шрифта стиля Normal.

## Примеры

Показывает, как указать ограничение на количество строк на каждой странице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите питч, а затем используйте его для установки количества строк на странице в этом разделе.
// Достаточно большой размер шрифта сдвинет некоторые строки на следующую страницу, чтобы избежать перекрытия символов.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
