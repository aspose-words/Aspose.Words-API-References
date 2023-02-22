---
title: TextColumnCollection.Item
second_title: Справочник по API Aspose.Words для .NET
description: TextColumnCollection свойство. Возвращает текстовый столбец по указанному индексу.
type: docs
weight: 30
url: /ru/net/aspose.words/textcolumncollection/item/
---
## TextColumnCollection indexer

Возвращает текстовый столбец по указанному индексу.

```csharp
public TextColumn this[int index] { get; }
```

### Примеры

Показывает, как создавать неравномерно расположенные столбцы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Определяем количество места, которое у нас есть для размещения столбцов.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Сделать первый столбец узким.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Устанавливаем второй столбец так, чтобы он занимал оставшееся пространство, доступное на полях страницы.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Смотрите также

* class [TextColumn](../../textcolumn/)
* class [TextColumnCollection](../)
* пространство имен [Aspose.Words](../../textcolumncollection/)
* сборка [Aspose.Words](../../../)


