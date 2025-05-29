---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder InsertParagraph 方法轻松增强您的文档，实现无缝段落分隔，提高可读性。
type: docs
weight: 450
url: /zh/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

在文档中插入段落分隔符。

```csharp
public Paragraph InsertParagraph()
```

### 返回值

刚刚插入的段落节点。它与[`CurrentParagraph`](../currentparagraph/)。

## 评论

当前段落格式由[`ParagraphFormat`](../paragraphformat/)属性被使用。

将当前段落一分为二。插入段落后，光标将位于新段落的开头。

如果无法在当前光标位置插入段落分隔符，则会引发异常。

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

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
