---
title: XpsSaveOptions.OutlineOptions
second_title: Aspose.Words for .NET API 参考
description: XpsSaveOptions 财产. 允许指定轮廓选项
type: docs
weight: 20
url: /zh/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

允许指定轮廓选项。

```csharp
public OutlineOptions OutlineOptions { get; }
```

### 评论

注意[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/)保存到 XPS 时选项将不起作用。

### 例子

演示如何限制将出现在已保存 XPS 文档大纲中的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1、2、3 级目录条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// 创建一个“XpsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// 输出 XPS 文档将包含大纲，即列出文档正文中的标题的目录。
// 单击此大纲中的条目将带我们到达其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，以从大纲中排除级别高于 2 的所有标题。
// 我们在上面插入的最后两个标题将不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### 也可以看看

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../xpssaveoptions/)
* 部件 [Aspose.Words](../../../)


