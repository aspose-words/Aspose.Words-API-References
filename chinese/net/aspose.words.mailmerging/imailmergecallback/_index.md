---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.MailMerging.IMailMergeCallback 优化您的邮件合并流程。获取实时通知，提升文档自动化效率。
type: docs
weight: 4490
url: /zh/net/aspose.words.mailmerging/imailmergecallback/
---
## IMailMergeCallback interface

如果您想在执行邮件合并时接收通知，请实现此接口。

```csharp
public interface IMailMergeCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | 当“胡子”文本标签被 MERGEFIELD 字段替换时调用。 |

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

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
