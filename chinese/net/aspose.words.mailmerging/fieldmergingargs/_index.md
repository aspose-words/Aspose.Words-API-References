---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMerging.FieldMergingArgs 类，用于在 MergeField 事件中无缝处理数据，增强您的文档处理体验。
type: docs
weight: 4460
url: /zh/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

为**合并字段**事件.

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | 返回[`Document`](../fieldmergingargsbase/document/)执行邮件合并的对象。 |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | 获取文档中指定的合并字段的名称。 |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | 获取代表当前合并字段的对象。 |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | 获取数据源中合并字段的名称。 |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | 从数据源获取或设置字段的值。 |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | 获取正在合并的记录的从零开始的索引。 |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | 获取当前合并操作的数据表名称，如果名称不可用，则获取空字符串。 |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | 获取或设置将插入到当前合并字段文档中的文本。 |

## 评论

这**合并字段**邮件合并期间，当文档中出现简单的邮件合并 字段时，将触发此事件。您可以响应此事件，返回 文本，以供邮件合并引擎插入到文档中。

## 例子

展示如何使用自定义回调执行邮件合并，以 HTML 文档的形式处理合并数据。

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// 如果邮件合并遇到名称以“html_”前缀开头的合并字段，
/// 此回调将其合并数据解析为 HTML 内容并将结果添加到 MERGEFIELD 的文档位置。
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// 当邮件合并将数据合并到 MERGEFIELD 时调用。
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // 将解析后的 HTML 数据添加到文档正文中。
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // 由于我们已经手动插入了合并的内容，
            // 我们不需要通过“Text”属性返回内容来响应此事件。
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // 什么也不做。
    }
}
```

### 也可以看看

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
