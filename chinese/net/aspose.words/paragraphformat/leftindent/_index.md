---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words for .NET
description: 使用 ParagraphFormat LeftIndent 属性轻松调整段落左缩进。自定义文本布局，提升可读性！
type: docs
weight: 180
url: /zh/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

获取或设置代表段落左缩进的值（以磅为单位）。

```csharp
public double LeftIndent { get; set; }
```

## 例子

展示如何配置段落格式来创建偏心文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 将文档构建器编写的所有文本居中，并设置缩进。
// 下面的缩进配置将创建一个在页面上不对称的文本主体。
// 我们将文本对齐到的“中心”是文本主体的中间，而不是页面的中间。
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
