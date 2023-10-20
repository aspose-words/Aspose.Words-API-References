---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge MergeWholeDocument 财产. 获取或设置一个值该值指示在执行区域邮件合并时是否更新整个文档中的字段 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

获取或设置一个值，该值指示在执行区域邮件合并时是否更新整个文档中的字段。

```csharp
public bool MergeWholeDocument { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

显示邮件合并与区域以及字段更新之间的关系。

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // 如果我们将“MergeWholeDocument”标志设置为“true”，
    // 与区域的邮件合并将更新文档中的每个字段。
    // 如果我们将“MergeWholeDocument”标志设置为“false”，则邮件合并将仅更新字段
    // 在邮件合并区域内，其名称与数据源表的名称相匹配。
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // 邮件合并只会更新邮件合并区域之外的 QUOTE 字段
    // 如果我们将“MergeWholeDocument”标志设置为“true”。
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// 创建一个包含邮件合并区域的文档，该区域属于名为“MyTable”的数据源。
/// 在此区域内插入一个 QUOTE 字段，并在其外部插入一个 QUOTE 字段。
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// 创建将在邮件合并中使用的数据表。
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
