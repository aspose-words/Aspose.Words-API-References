---
title: ParagraphFormat.AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 获取或设置一个标志指示是否在当前段落的拉丁文本区域 和东亚文本区域之间自动调整字符间距
type: docs
weight: 10
url: /zh/net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

获取或设置一个标志，指示是否在当前段落的拉丁文本区域 和东亚文本区域之间自动调整字符间距。

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
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

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


