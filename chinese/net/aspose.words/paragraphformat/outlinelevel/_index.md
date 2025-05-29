---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words for .NET
description: 探索 ParagraphFormat OutlineLevel 属性，轻松定义文档中的段落层次结构，增强组织性和可读性。
type: docs
weight: 260
url: /zh/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

指定文档中段落的大纲级别。

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## 例子

展示如何配置段落大纲级别以创建可折叠文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 每个段落都有一个 OutlineLevel，可以是 1 到 9 之间的任意数字，或者默认的“BodyText”值。
// 将属性设置为其中一个数字值将显示一个向左的箭头
// 段落的开头。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// 1 级为最高级别。如果一个级别较高的段落下方有一个级别较低的段落，
// 折叠较高级别的段落将会折叠较低级别的段落。
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// 两个同级别的段落不会互相折叠，
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
