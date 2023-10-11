---
title: FieldMergingArgs.Text
second_title: Aspose.Words for .NET API 参考
description: FieldMergingArgs 财产. 获取或设置将插入当前合并字段文档中的文本
type: docs
weight: 10
url: /zh/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

获取或设置将插入当前合并字段文档中的文本。

```csharp
public string Text { get; set; }
```

### 评论

当您的事件处理程序被调用时，该属性被设置为`无效的`。

如果您将文本保留为`无效的`，邮件合并引擎将插入[`FieldValue`](../../fieldmergingargsbase/fieldvalue/)代替合并字段。

如果将 Text 设置为任何字符串（包括空），则该字符串将插入到文档中代替合并字段。

### 例子

演示如何使用自定义回调执行邮件合并，该回调处理 HTML 文档形式的合并数据。

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
/// 如果邮件合并遇到名称以“html_”前缀开头的MERGEFIELD，
/// 此回调将其合并数据解析为 HTML 内容，并将结果添加到 MERGEFIELD 的文档位置。
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
        // 没做什么。
    }
}
```

### 也可以看看

* class [FieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../fieldmergingargs/)
* 部件 [Aspose.Words](../../../)


