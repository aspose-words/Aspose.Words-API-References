---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat AddSpaceBetweenFarEastAndDigit 财产. 获取或设置一个标志指示当前段落中数字的regions 与东亚文本区域之间的字符间距是否自动调整 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

获取或设置一个标志，指示当前段落中数字的regions 与东亚文本区域之间的字符间距是否自动调整。

```csharp
public bool AddSpaceBetweenFarEastAndDigit { get; set; }
```

## 例子

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

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
