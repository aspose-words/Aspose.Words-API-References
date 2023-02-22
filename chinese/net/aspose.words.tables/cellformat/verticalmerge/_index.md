---
title: CellFormat.VerticalMerge
second_title: Aspose.Words for .NET API 参考
description: CellFormat 财产. 指定单元格如何垂直与其他单元格合并
type: docs
weight: 120
url: /zh/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

指定单元格如何垂直与其他单元格合并。

```csharp
public CellMerge VerticalMerge { get; set; }
```

### 评论

只有左右边界相同的单元格才能垂直合并。

垂直合并单元格时，合并单元格的显示区域合并。 合并区域用于显示第一个垂直合并单元格 的内容，其他所有垂直合并单元格必须为空。

### 例子

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

显示如何垂直合并表格单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在第一行的第一列中插入一个单元格。
// 此单元格将是一系列垂直合并单元格中的第一个。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// 在第一行的第二列中插入一个单元格，然后结束该行。
// 另外，将构建器配置为在创建的单元格中禁用垂直合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

// 在第二行的第一列中插入一个单元格。 
// 我们不会添加文本内容，而是将此单元格与我们在上面直接添加的第一个单元格合并。
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// 在第二行的第二列插入另一个独立的单元格。
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
* 命名空间 [Aspose.Words.Tables](../../cellformat/)
* 部件 [Aspose.Words](../../../)


