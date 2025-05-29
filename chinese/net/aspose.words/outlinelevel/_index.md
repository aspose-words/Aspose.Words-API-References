---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.OutlineLevel 枚举，轻松管理文档中的段落大纲级别，以增强组织性和清晰度。
type: docs
weight: 5060
url: /zh/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

指定文档中段落的大纲级别。

```csharp
public enum OutlineLevel
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Level1 | `0` | 该段落位于大纲级别 1（最顶层）。 |
| Level2 | `1` | 该段落处于大纲级别 2。 |
| Level3 | `2` | 该段落处于大纲级别 3。 |
| Level4 | `3` | 该段落处于大纲级别 4。 |
| Level5 | `4` | 该段落处于大纲级别 5。 |
| Level6 | `5` | 该段落处于大纲级别 6。 |
| Level7 | `6` | 该段落处于大纲级别 7。 |
| Level8 | `7` | 该段落处于大纲级别 8。 |
| Level9 | `8` | 该段落处于大纲级别 9。 |
| BodyText | `9` | 该段落与正文处于同一级别。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
