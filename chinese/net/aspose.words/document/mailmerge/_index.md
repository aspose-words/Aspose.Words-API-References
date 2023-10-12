---
title: Document.MailMerge
second_title: Aspose.Words for .NET API 参考
description: Document 财产. 返回一个MailMerge代表文档邮件合并功能的对象
type: docs
weight: 260
url: /zh/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

返回一个[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/)代表文档邮件合并功能的对象。

```csharp
public MailMerge MailMerge { get; }
```

### 例子

演示如何使用数据表中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 下面是使用 DataTable 作为邮件合并数据源的两种方法。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - 使用表的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// 创建邮件合并源文档。
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### 也可以看看

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


