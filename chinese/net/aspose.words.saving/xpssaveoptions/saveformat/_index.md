---
title: XpsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: 探索 XpsSaveOptions 的 SaveFormat 属性，它定义了文档的保存方式。确保最佳的 XPS 格式，实现无缝文档处理！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/xpssaveoptions/saveformat/
---
## XpsSaveOptions.SaveFormat property

指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是Xps.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## 例子

展示如何限制已保存 XPS 文档大纲中出现的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1、2 和 3 级目录条目的标题。
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

// 输出的 XPS 文档将包含一个大纲，即列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，以从大纲中排除所有级别高于 2 的标题。
// 我们上面插入的最后两个标题将不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
