---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions 的 NavigationMapLevel 属性，控制 EPUB、MOBI 和 AZW3 导出格式中的标题级别。最大化内容的可见性！
type: docs
weight: 390
url: /zh/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

指定导出为 EPUB、MOBI 或 AZW3 格式时，导航地图中填充的标题的最大层级。默认值为`3`.

```csharp
public int NavigationMapLevel { get; set; }
```

## 评论

导航图允许用户代理提供一种便捷的文档结构导航方式。 通常，导航点与文档中的标题相对应。为了填充标题至以下级别**北** 将此值分配给`NavigationMapLevel`。

默认情况下，标题分为三个级别：段落、样式**标题 1**，**标题 2** 和**标题 3**. 您可以将此属性设置为从 1 到 9 的值，以请求相应的最大级别。 将其设置为零会将导航图减少为仅文档根目录或文档部分的根目录。

## 例子

展示如何生成 Azw3 文档的目录。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

展示如何为 Mobi 文档生成目录。

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

展示如何过滤已保存的 Epub 文档导航面板中出现的标题。

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

// Epub 读者通常会为他们的文档创建目录。
// 文档中每个具有“标题”样式的段落都会在此目录中创建一个条目。
 // 我们可以使用“NavigationMapLevel”属性来设置最大标题级别。
// Epub 阅读器不会将高于我们指定级别的标题添加到内容表中。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// 我们的文档有六个标题，其中两个高于 2 级。
// 本文档的目录将有四个条目。
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
