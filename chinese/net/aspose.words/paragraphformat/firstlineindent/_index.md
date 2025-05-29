---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words for .NET
description: 了解如何使用 ParagraphFormat FirstLineIndent 属性轻松自定义文档中的第一行或悬挂缩进，以提高可读性。
type: docs
weight: 120
url: /zh/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

获取或设置第一行或悬挂缩进的值（以磅为单位）。

使用正值设置首行缩进，使用负值设置悬挂缩进。

```csharp
public double FirstLineIndent { get; set; }
```

## 例子

展示如何在文档中插入段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

//“Writeln”方法在附加文本后结束段落
// 然后开始新的一行，添加一个新段落。
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
