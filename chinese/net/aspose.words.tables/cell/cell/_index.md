---
title: Cell
linktitle: Cell
articleTitle: Cell
second_title: Aspose.Words for .NET
description: 探索 Cell 构造函数，轻松创建新的 Cell 类实例。简化您的编码流程，提升开发效率！
type: docs
weight: 10
url: /zh/net/aspose.words.tables/cell/cell/
---
## Cell constructor

初始化[`Cell`](../)类.

```csharp
public Cell(DocumentBase doc)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | DocumentBase | 所有者文件。 |

## 评论

什么时候[`Cell`](../)已创建，它属于指定文档，但尚未成为文档的一部分，并且[`ParentNode`](../../../aspose.words/node/parentnode/)是`无效的`。

附加[`Cell`](../)文档使用[`InsertAfter`](../../../aspose.words/compositenode/insertafter/)或者[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)在要插入单元格的行上输入 。

## 例子

展示如何在不使用文档构建器的情况下构建嵌套表。

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // 创建具有三行四列的外部表格，然后将其添加到文档中。
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // 创建另一个具有两行两列的表格，然后将其插入到第一个表格的第一个单元格中。
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// 在文档中创建一个新表格，其中包含给定的尺寸和每个单元格中的文本。
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

    // 您可以使用“标题”和“描述”属性分别向表中添加标题和描述。
    // 在我们使用这些属性之前，表必须至少有一行。
    // 这些属性对于符合 ISO / IEC 29500 的 .docx 文档有意义（参见 OoxmlCompliance 类）。
    // 如果我们将文档保存为 ISO/IEC 29500 之前的格式，Microsoft Word 将忽略这些属性。
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### 也可以看看

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
