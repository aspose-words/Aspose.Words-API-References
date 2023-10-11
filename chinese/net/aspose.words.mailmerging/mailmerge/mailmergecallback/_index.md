---
title: MailMerge.MailMergeCallback
second_title: Aspose.Words for .NET API 参考
description: MailMerge 财产. 允许在邮件合并期间处理特定事件
type: docs
weight: 40
url: /zh/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

允许在邮件合并期间处理特定事件。

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

### 例子

演示如何定义用于在邮件合并期间处理事件的自定义逻辑。

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 插入两个引用数据源中两列的邮件合并标签。
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // 创建一个仅包含合并标记引用的列之一的数据源。
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // 配置我们的邮件合并以使用替代邮件合并标签。
    doc.MailMerge.UseNonMergeFields = true;

    // 然后，确保邮件合并会转换标签，比如我们的“LastName”标签，
    // 进入合并文档中的 MERGEFIELD。
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// 计算邮件合并替换无法使用 MERGEFIELD 填充数据的邮件合并标记的次数。
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

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


