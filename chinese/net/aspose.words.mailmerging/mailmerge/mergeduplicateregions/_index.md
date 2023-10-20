---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge MergeDuplicateRegions 财产. 获取或设置一个值该值指示在针对数据源或仅第一个区域执行邮件合并时是否应合并具有数据源 名称的所有文档邮件合并区域 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

获取或设置一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时是否应合并具有数据源 名称的所有文档邮件合并区域。

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

演示如何使用重复的邮件合并区域。

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // 如果我们将“MergeDuplicateRegions”属性设置为“false”，则邮件合并将影响第一个区域，
    // 而第二个的 MERGEFIELD 将保留在合并前状态。
    // 为了像这样合并两个区域，
    // 我们必须对同名的表执行两次邮件合并。
    // 如果我们将“MergeDuplicateRegions”属性设置为“true”，则邮件合并将影响两个区域。
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// 返回包含两个重复邮件合并区域的文档（在“TableStart/End”标记中共享相同的名称）。
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// 创建一个一行两列的数据表。
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
