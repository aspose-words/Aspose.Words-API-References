---
title: Table.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words for .NET
description: 发现表格标题属性，轻松设置或修改表格的标题，以提高可访问性和增强数据表示。
type: docs
weight: 320
url: /zh/net/aspose.words.tables/table/title/
---
## Table.Title property

获取或设置此表的标题。 它提供了表中包含的信息的替代文本表示。

```csharp
public string Title { get; set; }
```

## 评论

默认值为空字符串。

此属性对于符合 ISO/IEC 29500 的 DOCX documents 有意义（[`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). 当保存为 ISO/IEC 29500 之前的格式时，该属性将被忽略。

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

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
