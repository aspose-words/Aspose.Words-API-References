---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Tables.CellMerge 枚举. 指定表格中的单元格如何与其他单元格合并 在 C#.
type: docs
weight: 6270
url: /zh/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

指定表格中的单元格如何与其他单元格合并。

```csharp
public enum CellMerge
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 单元格未合并。 |
| First | `1` | 单元格是合并单元格范围中的第一个单元格。 |
| Previous | `2` | 单元格水平或垂直合并到前一个单元格。 |

## 例子

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

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
