---
title: Paragraph.IsEndOfDocument
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 如果该段落是文档最后一部分的最后一段则为 True
type: docs
weight: 60
url: /zh/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

如果该段落是文档最后一部分的最后一段，则为 True。

```csharp
public bool IsEndOfDocument { get; }
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

// “Writeln”方法在附加文本后结束段落
// 然后开始一个新行，添加一个新段落。
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### 也可以看看

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


