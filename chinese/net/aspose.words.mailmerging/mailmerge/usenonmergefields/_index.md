---
title: MailMerge.UseNonMergeFields
second_title: Aspose.Words for .NET API 参考
description: MailMerge 财产. 为真时指定除了 MERGEFIELD 字段外邮件合并到一些其他类型的字段中 也合并到fieldName标签中
type: docs
weight: 150
url: /zh/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

为真时，指定除了 MERGEFIELD 字段外，邮件合并到一些其他类型的字段中， 也合并到“{{fieldName}}”标签中。

```csharp
public bool UseNonMergeFields { get; set; }
```

### 评论

通常，邮件合并只在 MERGEFIELD 字段中执行，但有几个客户使用其他字段构建了他们的 reports ，并以这种方式创建了许多文档。为了简化迁移（并且因为 this 方法被多个客户独立使用），引入了将邮件合并到其他字段的能力。

什么时候 **使用非合并字段**设置为 true，Aspose.Words 会将邮件合并到以下字段中：

MERGEFIELD 字段名

MACROBUTTON NOMACRO 字段名

IF 0 = 0 "{字段名}" ""

还有，当 **用户非合并字段**设置为 true，Aspose.Words 会将邮件合并到文本 tags "{{fieldName}}" 中。这些不是字段，而只是文本标签。

### 例子

显示如何保留在邮件合并期间未使用的替代邮件合并标签的外观。

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

    // 默认情况下，邮件合并将表中每一行的数据放入 MERGEFIELD 中，这些名称为该表中的列命名。 
    // 我们的文档没有这样的字段，但它确实有用大括号括起来的明文标签。
    // 如果我们将“PreserveUnusedTags”标志设置为“true”，我们可以将这些标签视为 MERGEFIELD
    // 允许我们的邮件合并在这些标签处插入来自数据源的数据。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”，
    // 邮件合并会将这些标签转换为 MERGEFIELD 并将它们留空。
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // 我们的文档有一个名为“Column2”的列的标记，该列在表中不存在。
    // 如果我们将“PreserveUnusedTags”标志设置为“false”， then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// 创建一个文档并添加两个可以在邮件合并期间充当 MERGEFIELD 的纯文本标签。
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
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


