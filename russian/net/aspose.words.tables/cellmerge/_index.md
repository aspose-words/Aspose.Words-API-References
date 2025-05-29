---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Tables.CellMerge для эффективного объединения ячеек таблиц. Улучшите макеты документов с помощью бесшовной интеграции и гибкости.
type: docs
weight: 7120
url: /ru/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Указывает, как ячейка в таблице объединяется с другими ячейками.

```csharp
public enum CellMerge
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Ячейка не объединена. |
| First | `1` | Ячейка является первой ячейкой в диапазоне объединенных ячеек. |
| Previous | `2` | Ячейка объединяется с предыдущей ячейкой по горизонтали или вертикали. |

## Примеры

Показывает, как объединить ячейки таблицы по горизонтали.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем ячейку в первый столбец первой строки.
// Эта ячейка будет первой в ряду горизонтально объединенных ячеек.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Вставьте ячейку во второй столбец первой строки. Вместо добавления текстового содержимого,
// мы объединим эту ячейку с первой ячейкой, которую мы добавили непосредственно слева.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// Вставляем еще две необъединенные ячейки во вторую строку.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Печатает тип слияния ячейки по горизонтали и вертикали.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Показывает, как объединить ячейки таблицы по вертикали.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем ячейку в первый столбец первой строки.
// Эта ячейка будет первой в ряду вертикально объединенных ячеек.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// Вставляем ячейку во второй столбец первой строки, затем завершаем строку.
// Также настройте конструктор так, чтобы отключить вертикальное объединение в созданных ячейках.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // Вставляем ячейку в первый столбец второй строки.
// Вместо добавления текстового содержимого мы объединим эту ячейку с первой ячейкой, которую мы добавили непосредственно выше.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// Вставляем еще одну независимую ячейку во второй столбец второй строки.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
