---
title: Enum CellVerticalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Tables.CellVerticalAlignment перечисление. Задает вертикальное выравнивание текста внутри ячейки таблицы.
type: docs
weight: 5980
url: /ru/net/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enumeration

Задает вертикальное выравнивание текста внутри ячейки таблицы.

```csharp
public enum CellVerticalAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Top | `0` | Текст выравнивается по верхнему краю ячейки. |
| Center | `1` | Текст выравнивается по середине ячейки. |
| Bottom | `2` | Текст выравнивается по нижнему краю ячейки. |

### Примеры

Показывает, как построить отформатированную таблицу 2x2.

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

// При построении таблицы построитель документов применит текущие значения свойств RowFormat/CellFormat
// к текущей строке/ячейке, в которой находится его курсор, и к любым новым строкам/ячейкам по мере их создания.
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

// На ранее добавленные строки и ячейки изменения форматирования построителя не влияют задним числом.
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


