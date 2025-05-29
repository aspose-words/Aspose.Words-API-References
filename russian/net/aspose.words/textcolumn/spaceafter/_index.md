---
title: TextColumn.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextColumn SpaceAfter, чтобы легко настроить интервал между столбцами в макете. Улучшите читаемость и дизайн с точностью!
type: docs
weight: 10
url: /ru/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Получает или задает расстояние между этим столбцом и следующим столбцом в точках. Не требуется для последнего столбца.

```csharp
public double SpaceAfter { get; set; }
```

## Примеры

Показывает, как создавать неравномерно расположенные столбцы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Определяем количество места, доступного для размещения столбцов.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Сделаем первый столбец узким.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Установите второй столбец так, чтобы он занимал оставшееся пространство на полях страницы.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Смотрите также

* class [TextColumn](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
