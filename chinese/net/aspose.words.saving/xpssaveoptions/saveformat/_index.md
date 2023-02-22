---
title: XpsSaveOptions.SaveFormat
second_title: Aspose.Words for .NET API 参考
description: XpsSaveOptions 财产. 指定使用此保存选项对象时文档将保存的格式 只能是Xps.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/xpssaveoptions/saveformat/
---
## XpsSaveOptions.SaveFormat property

指定使用此保存选项对象时文档将保存的格式。 只能是Xps.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### 例子

显示如何限制将出现在已保存 XPS 文档大纲中的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可以用作级别 1、2 和 3 的 TOC 条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// 创建一个“XpsSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .XPS。
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// 输出的 XPS 文档将包含一个大纲，一个列出文档正文中标题的目录。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，从大纲中排除所有级别高于2的标题。
// 我们在上面插入的最后两个标题不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../xpssaveoptions/)
* 部件 [Aspose.Words](../../../)


