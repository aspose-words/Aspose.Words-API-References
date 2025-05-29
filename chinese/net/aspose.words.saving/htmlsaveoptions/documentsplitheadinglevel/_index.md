---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions 的 DocumentSplitHeadingLevel 优化文档拆分。控制标题级别以实现更佳的组织。默认设置为 2。
type: docs
weight: 90
url: /zh/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

指定拆分文档的最大标题级别。 默认值为`2`.

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## 评论

什么时候[`DocumentSplitCriteria`](../documentsplitcriteria/)包括HeadingParagraph 并且此属性设置为 1 到 9 之间的值，则文档将在使用 格式化的段落处拆分**标题 1**，**标题 2**，**标题 3**等样式直至指定的标题级别。

默认情况下，仅**标题 1**和**标题 2**段落导致文档被分割。 将此属性设置为零将导致文档根本不在标题段落处分割。

## 例子

展示如何根据标题将输出 HTML 文档分成几个部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们使用“标题”样式格式化的每个段落都可以作为标题。
// 每个标题也可能有一个标题级别，由其标题样式的数量决定。
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

// 创建一个 HtmlSaveOptions 对象并将拆分条件设置为“HeadingParagraph”。
// 这些标准将把文档按“标题”样式的段落拆分成几个较小的文档，
// 并将每个文档保存在本地文件系统中的单独 HTML 文件中。
// 我们还将设置最大标题级别，将文档拆分为 2 个。
// 保存文档将按照 1 级和 2 级标题进行拆分，但不按照 3 级到 9 级标题进行拆分。
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// 我们的文档有 1 - 2 级的四个标题。其中一个标题不会
// 分割点，因为它位于文档的开头。
// 保存操作将在三个地方将我们的文档拆分为四个较小的文档。
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
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
