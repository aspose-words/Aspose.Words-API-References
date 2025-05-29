---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words for .NET
description: 发现 MailMerge PreserveUnusedTags 属性以有效管理未使用的胡须标签，增强文档自动化流程。
type: docs
weight: 80
url: /zh/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

获取或设置一个值，指示是否应保留未使用的“胡子”标签。

```csharp
public bool PreserveUnusedTags { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何保留邮件合并期间未使用的替代邮件合并标签的外观。

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // 默认情况下，邮件合并将表格中每一行的数据放入 MERGEFIELDs 中，MERGEFIELDs 为该表中的列命名。
    // 我们的文档没有这样的字段，但它确实有用花括号括起来的纯文本标签。
    // 如果我们将“PreserveUnusedTags”标志设置为“true”，我们可以将这些标签视为 MERGEFIELD
    // 允许我们的邮件合并在这些标签处插入来自数据源的数据。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”，
    // 邮件合并将把这些标签转换为 MERGEFIELDs 并保持未填充状态。
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // 我们的文档有一个名为“Column2”的列的标签，但表中并不存在该列。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”， then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// 创建一个文档并添加两个纯文本标签，它们可以在邮件合并期间充当 MERGEFIELD。
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // 仅当我们将其设置为 true 时，我们的标签才会注册为邮件合并数据的目的地。
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// 创建一个只有一列的简单数据表。
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### 也可以看看

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
