---
title: KeepTogether
second_title: Aspose.Words for .NET API 参考
description: 如果段落中的所有行都保留在同一页上则为真
type: docs
weight: 150
url: /zh/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

如果段落中的所有行都保留在同一页上，则为真。

```csharp
public bool KeepTogether { get; set; }
```

### 例子

演示如何在文档中插入段落。

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

// “Writeln”方法在追加文本后结束段落
// 然后开始一个新行，添加一个新段落。
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### 也可以看看

* class [ParagraphFormat](../../paragraphformat)
* 命名空间 [Aspose.Words](../../paragraphformat)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
