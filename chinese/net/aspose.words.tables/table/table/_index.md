---
title: Table.Table
second_title: Aspose.Words for .NET API 参考
description: Table 构造函数. 初始化 桌子类.
type: docs
weight: 10
url: /zh/net/aspose.words.tables/table/table/
---
## Table constructor

初始化 **桌子**类.

```csharp
public Table(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

### 评论

什么时候 **桌子**被创建，它属于指定的文档，但不是 还不是文档的一部分，并且 **父节点**一片空白。

追加 **桌子**在要插入表格的故事上使用 InsertAfter 或 InsertBefore 文档。

### 例子

显示如何创建表。

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// 表格包含行，其中包含单元格，其中可能有段落
// 带有典型元素，例如运行、形状，甚至其他表格。
// 在表上调用“EnsureMinimum”方法将确保
// 表格至少有一行、一个单元格和一个段落。
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// 在表格第一行的第一个调用中添加文本。
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

展示如何在不使用文档构建器的情况下构建嵌套表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // 创建三行四列的外部表，然后将其添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // 创建另一个包含两行两列的表，然后将其插入到第一个表的第一个单元格中。
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

    // 您可以使用“标题”和“描述”属性分别为表格添加标题和描述。
    // 在我们可以使用这些属性之前，表格必须至少有一行。
    // 这些属性对于符合 ISO/IEC 29500 的 .docx 文档有意义（请参阅 OoxmlCompliance 类）。
    // 如果我们将文档保存为 pre-ISO/IEC 29500 格式，Microsoft Word 会忽略这些属性。
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


