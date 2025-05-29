---
title: TextColumnCollection.EvenlySpaced
linktitle: EvenlySpaced
articleTitle: EvenlySpaced
second_title: Aspose.Words для .NET
description: Откройте для себя свойство EvenlySpaced TextColumnCollection, которое обеспечивает текстовые столбцы одинаковой ширины для чистого, организованного макета. Улучшите свой дизайн без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words/textcolumncollection/evenlyspaced/
---
## TextColumnCollection.EvenlySpaced property

Истина, если текстовые столбцы имеют одинаковую ширину и равномерно распределены.

```csharp
public bool EvenlySpaced { get; set; }
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

* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
