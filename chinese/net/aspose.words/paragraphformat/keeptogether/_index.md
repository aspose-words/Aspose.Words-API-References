---
title: ParagraphFormat.KeepTogether
linktitle: KeepTogether
articleTitle: KeepTogether
second_title: Aspose.Words for .NET
description: 发现 ParagraphFormat KeepTogether 属性，确保所有行都集中在一页上，以提高文档的可读性和专业呈现效果。
type: docs
weight: 160
url: /zh/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

如果段落中的所有行都保留在同一页面上，则为真。

```csharp
public bool KeepTogether { get; set; }
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
