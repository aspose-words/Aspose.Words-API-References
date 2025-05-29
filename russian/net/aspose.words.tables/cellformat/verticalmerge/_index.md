---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat VerticalMerge для бесшовного вертикального объединения ячеек в электронных таблицах. Улучшите организацию и представление данных без усилий!
type: docs
weight: 130
url: /ru/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

Указывает, как ячейка объединяется с другими ячейками по вертикали.

```csharp
public CellMerge VerticalMerge { get; set; }
```

## Примечания

Ячейки можно объединять по вертикали только в том случае, если их левая и правая границы идентичны.

При вертикальном объединении ячеек области отображения объединенных ячеек объединяются. Объединенная область используется для отображения содержимого первой вертикально объединенной ячейки , а все остальные вертикально объединенные ячейки должны быть пустыми.

## Примеры

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

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
