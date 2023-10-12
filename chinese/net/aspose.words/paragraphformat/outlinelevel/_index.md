---
title: ParagraphFormat.OutlineLevel
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 指定文档中段落的大纲级别
type: docs
weight: 250
url: /zh/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

指定文档中段落的大纲级别。

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### 例子

演示如何配置段落大纲级别以创建可折叠文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 每个段落都有一个 OutlineLevel，可以是 1 到 9 之间的任意数字，或者使用默认的“BodyText”值。
// 将属性设置为编号值之一将显示向左的箭头
// 段落开头。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// 级别 1 是最顶层。如果较高级别的段落下面有较低级别的段落，
// 折叠较高级别的段落将折叠较低级别的段落。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// 同一层级的两个段落不会互相折叠，
// 并且箭头不会折叠它们指向的段落。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// 默认的“BodyText”值是最低的，任何级别的段落都可以折叠。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### 也可以看看

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


