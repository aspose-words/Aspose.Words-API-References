---
title: IMailMergeCallback Interface
linktitle: IMailMergeCallback
articleTitle: IMailMergeCallback
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.MailMerging.IMailMergeCallback 界面. 如果您想在执行邮件合并时接收通知请实现此接口 在 C#.
type: docs
weight: 3800
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
| [TagsReplaced](../../aspose.words.mailmerging/imailmergecallback/tagsreplaced/)() | 当“mustache”文本标记替换为 MERGEFIELD 字段时调用。 |

## 例子

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

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
