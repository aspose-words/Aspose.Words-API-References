---
title: TextColumn.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words для .NET
description: Отрегулируйте свойство TextColumn Width, чтобы легко настроить ширину текстового столбца в пунктах для улучшенного управления макетом и удобства чтения.
type: docs
weight: 20
url: /ru/net/aspose.words/textcolumn/width/
---
## TextColumn.Width property

Возвращает или задает ширину текстового столбца в пунктах.

```csharp
public double Width { get; set; }
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
