---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words for .NET
description: 了解如何使用 MailMerge UseWholeParagraphAsRegion 属性来增强邮件合并区域，确保完全控制内容包含。
type: docs
weight: 160
url: /zh/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

获取或设置一个值，指示整个段落是否**表开始**或者**桌尾**field 或之间的特定范围**表开始**和**桌尾**字段应包含在邮件合并区域中。

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## 评论

默认值为`真的`.

## 例子

显示邮件合并区域和段落之间的关系。

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // 默认情况下，一个段落最多只能属于一个邮件合并区域。
    // 我们的文档内容不符合这些标准。
    // 如果我们将“UseWholeParagraphAsRegion”标志设置为“true”，
    // 对此文档运行邮件合并将引发异常。
    // 如果我们将“UseWholeParagraphAsRegion”标志设置为“false”，
    // 我们将能够对该文档执行邮件合并。
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // 邮件合并填充了我们的第一个区域，而第二个区域未被使用
    // 因为它是违反规则的区域。
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// 创建一个其中两个邮件合并区域共享一个段落的文档。
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// 创建一个可以在邮件合并期间填充一个区域的数据表。
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
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
