---
title: TextColumn.SpaceAfter
second_title: Справочник по API Aspose.Words для .NET
description: TextColumn свойство. Получает или задает расстояние между этим столбцом и следующим столбцом в пунктах. Не требуется для последнего столбца.
type: docs
weight: 10
url: /ru/net/aspose.words/textcolumn/spaceafter/
---
## TextColumn.SpaceAfter property

Получает или задает расстояние между этим столбцом и следующим столбцом в пунктах. Не требуется для последнего столбца.

```csharp
public double SpaceAfter { get; set; }
```

### Примеры

Показывает, как создавать столбцы с неравномерным расположением друг от друга.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Определим количество свободного места для размещения столбцов.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Установите узкий первый столбец.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Установите второй столбец так, чтобы он занял оставшееся пространство, доступное в пределах полей страницы.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Смотрите также

* class [TextColumn](../)
* пространство имен [Aspose.Words](../../textcolumn/)
* сборка [Aspose.Words](../../../)


