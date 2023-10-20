---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: 用于 .NET 的 Aspose.Words
description: CellFormat VerticalMerge 财产. 指定单元格如何与其他单元格垂直合并 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

指定单元格如何与其他单元格垂直合并。

```csharp
public CellMerge VerticalMerge { get; set; }
```

## 评论

仅当单元格的左右边界相同时，才能垂直合并。

垂直合并单元格时，合并单元格的显示区域将被合并。 合并区域用于显示第一个垂直合并单元格 的内容，所有其他垂直合并单元格必须为空。

## 例子

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

演示如何垂直合并表格单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将单元格插入第一行的第一列。
// 该单元格将是一系列垂直合并单元格中的第一个。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// 将一个单元格插入第一行的第二列，然后结束该行。
// 另外，配置构建器以禁用创建的单元格中的垂直合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // 将单元格插入第二行第一列。
// 我们不会添加文本内容，而是将此单元格与我们在上面直接添加的第一个单元格合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// 在第二行第二列插入另一个独立单元格。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### 也可以看看

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
