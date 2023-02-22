---
title: Cell.CellFormat
second_title: Справочник по API Aspose.Words для .NET
description: Cell свойство. Предоставляет доступ к свойствам форматирования ячейки.
type: docs
weight: 20
url: /ru/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Предоставляет доступ к свойствам форматирования ячейки.

```csharp
public CellFormat CellFormat { get; }
```

### Примеры

Показывает, как изменить форматирование ячейки таблицы.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Используйте свойство CellFormat ячейки, чтобы установить форматирование, которое изменяет внешний вид этой ячейки.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Показывает, как объединить строки из двух таблиц в одну.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Ниже приведены два способа получения таблицы из документа.
// 1 - Из коллекции "Таблицы" узла Body:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Используя метод "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Добавляем все строки из текущей таблицы в следующую.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Удалить пустой контейнер таблицы.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
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

// Используйте свойство "RowFormat" первой строки, чтобы изменить форматирование
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

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../cell/)
* сборка [Aspose.Words](../../../)


