---
title: CellFormat.HorizontalMerge
linktitle: HorizontalMerge
articleTitle: HorizontalMerge
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CellFormat HorizontalMerge, позволяющее легко объединять ячейки по горизонтали, улучшая компоновку и организацию вашей электронной таблицы.
type: docs
weight: 50
url: /ru/net/aspose.words.tables/cellformat/horizontalmerge/
---
## CellFormat.HorizontalMerge property

Указывает, как ячейка будет объединена по горизонтали с другими ячейками в строке.

```csharp
public CellMerge HorizontalMerge { get; set; }
```

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

### Смотрите также

* property [VerticalMerge](../verticalmerge/)
* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
