---
title: DocumentBuilder.InsertHtml
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将 HTML 字符串插入文档中
type: docs
weight: 360
url: /zh/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(string) {#inserthtml}

将 HTML 字符串插入文档中。

```csharp
public void InsertHtml(string html)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | String | 要插入到文档中的 HTML 字符串。 |

### 评论

您可以使用此方法插入 HTML 片段或整个 HTML 文档。

### 例子

演示如何使用文档生成器将 html 内容插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// 插入 HTML 代码会将每个元素的格式解析为等效的文档文本格式。
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

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

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertHtml(string, bool) {#inserthtml_2}

将 HTML 字符串插入文档中。

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| html | String | 要插入到文档中的 HTML 字符串。 |
| useBuilderFormatting | Boolean | 指示是否在中指定格式的值[`DocumentBuilder`](../) 用作从 HTML 导入的文本的基本格式。 |

### 评论

您可以使用此方法插入 HTML 片段或整个 HTML 文档。

当*useBuilderFormatting*是`错误的`, [`DocumentBuilder`](../)格式被忽略，插入的 text 的格式基于默认的 HTML 格式。结果，文本看起来就像在浏览器中呈现的一样。

当*useBuilderFormatting*是`真的` , 插入文本的格式基于[`DocumentBuilder`](../)格式， 并且文本看起来好像是用[`Write`](../write/).

### 例子

演示如何在插入 HTML 内容时应用文档生成器的格式设置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为构建器设置文本对齐方式，插入具有指定对齐方式的 HTML 段落和不具有指定对齐方式的 HTML 段落。
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// 第一个段落指定了对齐方式。当InsertHtml解析HTML代码时，
// HTML 代码中的段落对齐值始终取代文档生成器的值。
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// 第二段没有指定对齐方式。可以填写其对齐值
// 由构建器的值取决于我们传递给 InsertHtml 方法的标志。
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertHtml(string, HtmlInsertOptions) {#inserthtml_1}

将 HTML 字符串插入到文档中。允许指定附加选项。

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

演示如何在插入 html 时使用选项。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// 默认情况下“DocumentBuilder.InsertHtml”插入一个以块级 HTML 元素结尾的 HTML 片段，
// 它通常会关闭该块级元素并插入段落分隔符。
// 结果，插入文档后会出现一个新的空段落。
// 如果我们指定“HtmlInsertOptions.RemoveLastEmptyParagraph”，那些多余的空段落将被删除。
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### 也可以看看

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


