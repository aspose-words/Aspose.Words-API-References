---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge UseNonMergeFields 财产. 当真的指定除了 MERGEFIELD 字段之外还会将邮件合并到其他一些类型的字段中并且 还执行到fieldName标签中 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

当`真的`，指定除了 MERGEFIELD 字段之外，还会将邮件合并到其他一些类型的字段中，并且 还执行到“{{fieldName}}”标签中。

```csharp
public bool UseNonMergeFields { get; set; }
```

## 评论

通常，邮件合并仅在 MERGEFIELD 字段中执行，但一些客户使用其他字段构建了 reporting ，并以这种方式创建了许多文档。为了简化迁移（并且因为 this 方法被多个客户独立使用），引入了将邮件合并到其他字段的功能。

什么时候`UseNonMergeFields`被设定为`真的`，Aspose.Words 将执行邮件合并到以下字段：

MERGEFIELD 字段名称

MACROBUTTON NOMACRO 字段名称

如果 0 = 0 "{FieldName}" ""

另外，当`UseNonMergeFields`被设定为`真的`，Aspose.Words 将执行邮件合并为文本tags “{{fieldName}}”。这些不是字段，而只是文本标签。

## 例子

演示如何保留在邮件合并期间未使用的备用邮件合并标记的外观。

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // 默认情况下，邮件合并将表中每一行的数据放入 MERGEFIELD 中，MERGEFIELD 命名该表中的列。
    // 我们的文档没有这样的字段，但它确实有用大括号括起来的纯文本标签。
    // 如果我们将“PreserveUnusedTags”标志设置为“true”，我们可以将这些标签视为 MERGEFIELD
    // 允许我们的邮件合并在这些标签处插入来自数据源的数据。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”，
    // 邮件合并会将这些标签转换为 MERGEFIELD 并将其保留为空。
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // 我们的文档有一个名为“Column2”的列的标签，该标签在表中不存在。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”， then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// 创建一个文档并添加两个纯文本标记，这些标记可以在邮件合并期间充当 MERGEFIELD。
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
/// 创建一个包含一列的简单数据表。
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

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
