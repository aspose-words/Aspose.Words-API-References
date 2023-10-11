---
title: Table.Table
second_title: Aspose.Words for .NET API 参考
description: Table 构造函数. 初始化一个新实例Table类.
type: docs
weight: 10
url: /zh/net/aspose.words.tables/table/table/
---
## Table constructor

初始化一个新实例[`Table`](../)类.

```csharp
public Table(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

### 评论

什么时候[`Table`](../)创建后，它属于指定文档，但还不是 文档的一部分并且[`ParentNode`](../../../aspose.words/node/parentnode/)是`无效的`。

追加[`Table`](../)到文档使用Node)或者Node) 位于您想要插入表格的故事上。

### 例子

展示如何创建表。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// 表格包含行，行包含单元格，单元格可能包含段落
// 具有典型元素，例如运行、形状，甚至其他表格。
// 在表上调用“EnsureMinimum”方法将确保
// 该表格至少有一行、一个单元格和一个段落。
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// 将文本添加到表第一行中的第一个调用。
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

演示如何在不使用文档生成器的情况下构建嵌套表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // 创建三行四列的外表，然后将其添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // 创建另一个包含两行和两列的表格，然后将其插入到第一个表格的第一个单元格中。
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// 在文档中创建一个新表格，每个单元格中具有给定的尺寸和文本。
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // 您可以使用“标题”和“描述”属性分别向表格添加标题和描述。
    // 在我们可以使用这些属性之前，表必须至少有一行。
    // 这些属性对于符合 ISO / IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
    // 如果我们将文档保存为 ISO/IEC 29500 之前的格式，Microsoft Word 将忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### 也可以看看

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


