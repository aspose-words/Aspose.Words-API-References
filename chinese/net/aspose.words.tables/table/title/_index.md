---
title: Table.Title
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取或设置此表的标题 它提供表中包含的信息的替代文本表示
type: docs
weight: 320
url: /zh/net/aspose.words.tables/table/title/
---
## Table.Title property

获取或设置此表的标题。 它提供表中包含的信息的替代文本表示。

```csharp
public string Title { get; set; }
```

### 评论

默认值为空字符串。

此属性对符合 ISO/IEC 29500 的 DOCX 文档有意义 ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). 当保存为 pre-ISO/IEC 29500 格式时，该属性将被忽略。

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

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


