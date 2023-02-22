---
title: Row.Row
second_title: Aspose.Words for .NET API 参考
description: Row 构造函数. 初始化 排类.
type: docs
weight: 10
url: /zh/net/aspose.words.tables/row/row/
---
## Row constructor

初始化 **排**类.

```csharp
public Row(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

### 评论

什么时候 **排**被创建，它属于指定的文档，但不是 还不是文档的一部分，并且 **父节点**一片空白。

追加 **排**在要插入行的表上使用 InsertAfter 或 InsertBefore 到文档中。

### 例子

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
* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../row/)
* 部件 [Aspose.Words](../../../)


