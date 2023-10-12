---
title: CellFormat.RightPadding
second_title: Справочник по API Aspose.Words для .NET
description: CellFormat свойство. Возвращает или задает количество места в пунктах которое нужно добавить справа от содержимого ячейки.
type: docs
weight: 90
url: /ru/net/aspose.words.tables/cellformat/rightpadding/
---
## CellFormat.RightPadding property

Возвращает или задает количество места (в пунктах), которое нужно добавить справа от содержимого ячейки.

```csharp
public double RightPadding { get; set; }
```

### Примеры

Показывает, как форматировать ячейки с помощью построителя документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Вставляем вторую ячейку, а затем настраиваем параметры заполнения текста ячейки.
// Построитель применит эти настройки к своей текущей ячейке, а затем создаст все новые ячейки.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// На первую ячейку не повлияла реконфигурация заполнения, и она по-прежнему содержит значения по умолчанию.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// Первая ячейка в выходном документе по-прежнему будет расти, чтобы соответствовать размеру соседней ячейки.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Смотрите также

* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../cellformat/)
* сборка [Aspose.Words](../../../)


