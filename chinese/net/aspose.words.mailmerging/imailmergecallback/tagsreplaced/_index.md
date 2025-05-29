---
title: IMailMergeCallback.TagsReplaced
linktitle: TagsReplaced
articleTitle: TagsReplaced
second_title: Aspose.Words for .NET
description: 了解 IMailMergeCallback TagsReplaced 方法如何通过使用 MERGEFIELD 字段无缝替换胡须文本来增强文档自动化。
type: docs
weight: 10
url: /zh/net/aspose.words.mailmerging/imailmergecallback/tagsreplaced/
---
## IMailMergeCallback.TagsReplaced method

当“胡子”文本标签被 MERGEFIELD 字段替换时调用。

```csharp
public void TagsReplaced()
```

## 例子

展示如何定义自定义逻辑来处理邮件合并期间的事件。

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入两个引用数据源中两列的邮件合并标签。
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // 创建一个仅包含合并标签引用的其中一列的数据源。
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // 配置我们的邮件合并以使用替代邮件合并标签。
    doc.MailMerge.UseNonMergeFields = true;

    // 然后，确保邮件合并将转换标签，例如我们的“LastName”标签，
    // 进入合并文档中的 MERGEFIELDs。
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// 计算邮件合并用无法用 MERGEFIELD 填充数据的邮件合并标签替换的次数。
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### 也可以看看

* property [UseNonMergeFields](../../mailmerge/usenonmergefields/)
* interface [IMailMergeCallback](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
