---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words for .NET
description: 使用 MergeDuplicateRegions 属性优化您的邮件合并流程。控制数据源区域的合并方式，实现高效的文档管理。
type: docs
weight: 60
url: /zh/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

获取或设置一个值，该值指示在执行针对数据源的区域邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域 ，还是仅合并第一个。

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何处理重复的邮件合并区域。

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // 如果我们将“MergeDuplicateRegions”属性设置为“false”，邮件合并将影响第一个区域，
    // 而第二个的 MERGEFIELD 将保持合并前的状态。
    // 为了使两个区域合并，
    // 我们必须在同名表上执行两次邮件合并。
    // 如果我们将“MergeDuplicateRegions”属性设置为“true”，则邮件合并将影响两个区域。
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// 返回包含两个重复邮件合并区域（在“TableStart/End”标签中共享相同名称）的文档。
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
/// 创建一个具有一行和两列的数据表。
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
