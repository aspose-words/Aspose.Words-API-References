---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat RightIndent 财产. 获取或设置表示段落正确缩进的值以磅为单位 在 C#.
type: docs
weight: 270
url: /zh/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

获取或设置表示段落正确缩进的值（以磅为单位）。

```csharp
public double RightIndent { get; set; }
```

## 例子

演示如何配置段落格式以创建偏离中心的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将文档构建器编写的所有文本居中，并设置缩进。
// 下面的缩进配置将创建一个不对称地位于页面上的文本正文。
// 我们将文本对齐的“中心”将是文本正文的中间，而不是页面的中间。
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
