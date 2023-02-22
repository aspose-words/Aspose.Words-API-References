---
title: CellFormat.HorizontalMerge
second_title: Aspose.Words for .NET API 参考
description: CellFormat 财产. 指定单元格如何与行中的其他单元格水平合并
type: docs
weight: 40
url: /zh/net/aspose.words.tables/cellformat/horizontalmerge/
---
## CellFormat.HorizontalMerge property

指定单元格如何与行中的其他单元格水平合并。

```csharp
public CellMerge HorizontalMerge { get; set; }
```

### 例子

显示如何水平合并表格单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在第一行的第一列中插入一个单元格。
// 此单元格将是一系列水平合并单元格中的第一个。
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// 在第一行的第二列中插入一个单元格。而不是添加文本内容，
// 我们将把这个单元格与我们直接添加到左边的第一个单元格合并。
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// 在第二行再插入两个未合并的单元格。
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

打印单元格的水平和垂直合并类型。

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows.OfType<Row>())
        foreach (Cell cell in row.Cells.OfType<Cell>())
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

### 也可以看看

* property [VerticalMerge](../verticalmerge/)
* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../cellformat/)
* 部件 [Aspose.Words](../../../)


