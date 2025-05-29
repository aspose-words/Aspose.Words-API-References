---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words for .NET
description: 了解 MailMerge 的 UnconditionalMergeFieldsAndRegions 属性如何通过合并不受条件限制的字段和区域来增强文档自动化。
type: docs
weight: 140
url: /zh/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

获取或设置一个值，该值指示合并字段和合并区域是否合并，而不管父 IF 字段的条件如何。

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## 评论

默认值为`错误的`.

## 例子

展示如何合并字段或区域，而不管父 IF 字段的条件如何。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入嵌套在 IF 字段内的 MERGEFIELD。
// 由于 IF 字段语句为假，因此不会显示 MERGEFIELD 的结果。
// MERGEFIELD 在邮件合并期间也不会接收任何数据。
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// 如果我们将“UnconditionalMergeFieldsAndRegions”标志设置为“true”，
// 我们的邮件合并将把数据插入到未显示的字段中，例如我们的 MERGEFIELD 以及所有其他字段。
// 如果我们将“UnconditionalMergeFieldsAndRegions”标志设置为“false”，
// 我们的邮件合并不会将数据插入到被带有错误语句的 IF 字段隐藏的 MERGEFIELDs 中。
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
