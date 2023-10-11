---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定分割文档的最大标题级别 默认值为2.
type: docs
weight: 90
url: /zh/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

指定分割文档的最大标题级别。 默认值为`2`.

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### 评论

什么时候[`DocumentSplitCriteria`](../documentsplitcriteria/)包括HeadingParagraph 并且此属性设置为 1 到 9 之间的值，文档将按使用 格式化的段落进行分割 **标题 1**, **标题 2**, **标题 3**等样式达到指定的标题级别。

默认情况下，仅 **标题 1**和 **标题 2**段落导致文档被分割。 将此属性设置为零将导致文档根本不会在标题段落处拆分。

### 例子

演示如何按标题将输出 HTML 文档拆分为多个部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们使用“标题”样式格式化的每个段落都可以用作标题。
// 每个标题还可以有一个标题级别，由其标题样式的数量决定。
// 下面的标题为 1-3 级。
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// 创建一个 HtmlSaveOptions 对象并将分割条件设置为“HeadingParagraph”。
// 这些条件会将具有“标题”样式的段落中的文档拆分为几个较小的文档，
// 并将每个文档保存在本地文件系统中的单独 HTML 文件中。
// 我们还将设置最大标题级别，将文档拆分为 2。
// 保存文档时会将其拆分为 1 级和 2 级标题，但不会拆分为 3 到 9 级标题。
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// 我们的文档有四个级别 1 - 2 的标题。其中一个标题不会是
// 分割点，因为它位于文档的开头。
// 保存操作会将我们的文档在三个地方分割成四个较小的文档。
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


