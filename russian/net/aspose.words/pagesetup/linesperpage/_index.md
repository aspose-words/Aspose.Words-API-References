---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words для .NET
description: PageSetup LinesPerPage свойство. Получает или задает количество строк на странице в сетке документа на С#.
type: docs
weight: 240
url: /ru/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Получает или задает количество строк на странице в сетке документа.

```csharp
public int LinesPerPage { get; set; }
```

## Примечания

Минимальное значение свойства — 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal . Минимальный шаг строки составляет 136 процентов от размера шрифта. Например, максимальное количество строк на странице страницы Letter с полями в один дюйм составляет 39.

По умолчанию свойство имеет значение, при котором шаг строки в 1,5 раза превышает размер шрифта стиля Обычный.

## Примеры

Показывает, как указать ограничение на количество строк, которое может иметь каждая страница.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите шаг, а затем используйте его, чтобы установить количество строк на странице в этом разделе.
// Достаточно большой размер шрифта переместит некоторые строки вниз на следующую страницу, чтобы избежать перекрытия символов.
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
