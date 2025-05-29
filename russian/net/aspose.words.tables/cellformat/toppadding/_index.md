---
title: CellFormat.TopPadding
linktitle: TopPadding
articleTitle: TopPadding
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat TopPadding, позволяющее настраивать интервал над содержимым ячеек в пунктах, улучшая макет и читабельность вашей электронной таблицы.
type: docs
weight: 110
url: /ru/net/aspose.words.tables/cellformat/toppadding/
---
## CellFormat.TopPadding property

Возвращает или задает размер пространства (в пунктах), добавляемого над содержимым ячейки.

```csharp
public double TopPadding { get; set; }
```

## Примеры

Показывает, как форматировать ячейки с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Вставьте вторую ячейку, а затем настройте параметры заполнения текста ячейки.
// Конструктор применит эти настройки к текущей ячейке и ко всем новым ячейкам, которые он создаст впоследствии.
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

// Первая ячейка не была затронута реконфигурацией заполнения и по-прежнему содержит значения по умолчанию.
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

// Первая ячейка в выходном документе все равно увеличится до размера соседней ячейки.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Смотрите также

* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
