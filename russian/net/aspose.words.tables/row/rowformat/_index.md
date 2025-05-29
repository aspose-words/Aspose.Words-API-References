---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Row RowFormat для легкого доступа к настраиваемым параметрам форматирования строк, что позволит без труда улучшить представление данных.
type: docs
weight: 110
url: /ru/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Предоставляет доступ к свойствам форматирования строки.

```csharp
public RowFormat RowFormat { get; }
```

## Примеры

Показывает, как изменить форматирование строки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Используйте свойство "RowFormat" первой строки, чтобы задать форматирование, которое изменяет внешний вид всей строки.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Показывает, как изменить формат строк и ячеек в таблице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Используйте свойство "RowFormat" первой строки для изменения форматирования
// содержимого всех ячеек в этой строке.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Используйте свойство «CellFormat» первой ячейки в последней строке, чтобы изменить форматирование содержимого этой ячейки.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Смотрите также

* class [RowFormat](../../rowformat/)
* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
