---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: Aspose.Words для .NET
description: Aspose.Words.Tables.AutoFitBehavior перечисление. Определяет как Aspose.Words изменяет размер таблицы при вызовеAutoFit метод на С#.
type: docs
weight: 6230
url: /ru/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Определяет, как Aspose.Words изменяет размер таблицы при вызове[`AutoFit`](../table/autofit/) метод.

```csharp
public enum AutoFitBehavior
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words включает опцию AutoFit, удаляет предпочтительную ширину из таблицы и всех ячеек, а затем обновляет макет таблицы. |
| AutoFitToWindow | `1` | Когда вы используете это значение, Aspose.Words включает опцию AutoFit, устанавливает предпочтительную ширину таблицы на 100%, удаляет предпочтительные ширины из всех ячеек, а затем обновляет макет таблицы. |
| FixedColumnWidths | `2` | Aspose.Words отключает опцию AutoFit и удаляет предпочтительный вариант из таблицы. |

## Примеры

Показывает, как построить новую таблицу с применением стиля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Мы должны вставить хотя бы одну строку, прежде чем устанавливать какое-либо форматирование таблицы.
builder.InsertCell();

// Установите используемый стиль таблицы на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формате .doc.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Частично применить стиль к функциям таблицы на основе предикатов, затем построить таблицу.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Показывает, как построить форматированную таблицу 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// При построении таблицы построитель документов будет применять текущие значения свойств RowFormat/CellFormat
// к текущей строке/ячейке, в которой находится курсор, и к любым новым строкам/ячейкам по мере их создания.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Ранее добавленные строки и ячейки не имеют обратной силы при изменении форматирования построителя.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
