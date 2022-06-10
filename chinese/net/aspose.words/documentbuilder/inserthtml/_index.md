---
title: InsertHtml
second_title: Aspose.Words for .NET API 参考
description: 将 HTML 字符串插入到文档中
type: docs
weight: 330
url: /zh/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(string) {#inserthtml}

将 HTML 字符串插入到文档中。

```csharp
public void InsertHtml(string html)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | String | 要插入到文档中的 HTML 字符串。 |

### 评论

您可以使用此方法插入 HTML 片段或整个 HTML 文档。

### 例子

展示如何使用文档构建器将 html 内容插入到文档中。

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
 /// 如果邮件合并遇到名称以“html_”前缀开头的MERGEFIELD,
 /// 此回调将其合并数据解析为 HTML 内容并将结果添加到 MERGEFIELD.
 的文档位置
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
     /// 当邮件合并将数据合并到 MERGEFIELD.
 时调用
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // 将解析后的 HTML 数据添加到文档的 body.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

             // 因为我们已经手动插入了合并的内容，
             // 我们不需要通过“Text”属性返回内容来响应这个事件。 
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
         // 什么都不做。
    }
}
```

显示如何使用处理 HTML 文档形式的合并数据的自定义回调执行邮件合并。

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
 /// 如果邮件合并遇到名称以“html_”前缀开头的MERGEFIELD,
 /// 此回调将其合并数据解析为 HTML 内容并将结果添加到 MERGEFIELD.
 的文档位置
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
     /// 当邮件合并将数据合并到 MERGEFIELD.
 时调用
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // 将解析后的 HTML 数据添加到文档的 body.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

             // 因为我们已经手动插入了合并的内容，
             // 我们不需要通过“Text”属性返回内容来响应这个事件。 
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
         // 什么都不做。
    }
}
```

### 也可以看看

* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

---

## InsertHtml(string, bool) {#inserthtml_2}

将 HTML 字符串插入到文档中。

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | String | 要插入到文档中的 HTML 字符串。 |
| useBuilderFormatting | Boolean | 一个值，指示是否在[`DocumentBuilder`](../../documentbuilder)中指定格式用作从 HTML 导入的文本的基本格式。 |

### 评论

您可以使用此方法插入 HTML 片段或整个HTML 文档。

当*useBuilderFormatting*为` false` , [`DocumentBuilder`](../../documentbuilder)格式被忽略，插入文本格式 基于默认值HTML 格式。因此，文本看起来就像在浏览器中呈现的一样。

当*useBuilderFormatting*为` true` , 插入文本的格式基于[`DocumentBuilder`](../../documentbuilder)格式, 和文本看起来好像是用[`Write`](../write)插入的。

### 例子

显示如何在插入 HTML 内容时应用文档构建器的格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为构建器设置文本对齐方式，插入一个带有指定对齐方式的 HTML 段落，一个没有。
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// 第一段指定了对齐方式。当 InsertHtml 解析 HTML 代码时，
// HTML 代码中的段落对齐值始终取代文档构建器的值。
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// 第二段没有指定对齐方式。它可以填充其对齐值
// 构建器的值取决于我们传递给 InsertHtml 方法的标志。
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### 也可以看看

* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

---

## InsertHtml(string, HtmlInsertOptions) {#inserthtml_1}

将 HTML 字符串插入到文档中。允许指定其他选项。

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | String | 要插入到文档中的 HTML 字符串。 |
| options | HtmlInsertOptions | 插入 HTML 字符串时使用的选项。 |

### 评论

您可以使用此方法插入 HTML 片段或整个 HTML 文档。

### 例子

展示如何在插入 html 时使用选项。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

 // 默认情况下，“DocumentBuilder.InsertHtml”插入一个以块级 HTML 元素结尾的 HTML 片段，
 // 它通常会关闭该块级元素并插入一个段落中断。
 // 结果，插入文档后出现一个新的空段落。
 // 如果我们指定“HtmlInsertOptions.RemoveLastEmptyParagraph”，那些多余的空段落将被删除。
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### 也可以看看

* enum [HtmlInsertOptions](../../htmlinsertoptions)
* class [DocumentBuilder](../../documentbuilder)
* 命名空间 [Aspose.Words](../../documentbuilder)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
