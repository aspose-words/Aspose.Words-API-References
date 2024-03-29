---
title: HtmlSaveOptions.EpubNavigationMapLevel
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别 默认值为3.
type: docs
weight: 110
url: /zh/net/aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/
---
## HtmlSaveOptions.EpubNavigationMapLevel property

指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别。 默认值为`3`.

```csharp
public int EpubNavigationMapLevel { get; set; }
```

### 评论

IDPF EPUB 格式的导航图允许用户代理通过文档结构提供简单的导航方式 。通常导航点对应于文档中的标题。 将标题填充到级别 **ñ**将此值分配给`EpubNavigationMapLevel`.

默认情况下，会填充三个级别的标题：样式段落 **标题 1**, **标题 2** 和 **标题 3**. 您可以将此属性设置为 1 到 9 的值以请求相应的最大级别。 将其设置为零会将导航图减少为仅文档根或文档部分的根。

### 例子

显示如何过滤出现在已保存 Epub 文档的导航面板中的标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们使用“标题”样式格式化的每个段落都可以用作标题。
// 每个标题也可能有一个标题级别，由其标题样式的数量决定。
// 下面的标题是 1-3 级的。
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

// Epub 阅读器通常会为其文档创建目录。
// 文档中每个带有“标题”样式的段落都会在这个目录中创建一个条目。
 // 我们可以使用“EpubNavigationMapLevel”属性来设置最大标题级别。
// Epub 阅读器不会将级别高于我们指定级别的标题添加到目录表中。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.EpubNavigationMapLevel = 2;

// 我们的文档有六个标题，其中两个在第 2 级以上。
// 此文档的目录将有四个条目。
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


