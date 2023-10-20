---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: 用于 .NET 的 Aspose.Words
description: Font Bidi 财产. 指定此运行的内容是否应具有从右到左的特征 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words/font/bidi/
---
## Font.Bidi property

指定此运行的内容是否应具有从右到左的特征。

```csharp
public bool Bidi { get; set; }
```

## 评论

启用此属性后，不得将其与强从左到右的文本一起使用。该条件下的任何行为均未指定。 此属性关闭后，不得与强从右到左文本一起使用。该条件下的任何行为均未指定。

当显示此运行的内容时，出于格式化 目的，所有字符都应被视为复杂脚本字符。这意味着[`BoldBi`](../boldbi/),[`ItalicBi`](../italicbi/),[`SizeBi`](../sizebi/)渲染此运行时将使用相应的字体名称 。

此外，当显示此运行的内容时，此属性充当字符 的从右到左覆盖，字符 被分类为“弱类型”和“中性类型”。

## 例子

演示如何为从右到左和从右到左的文本定义单独的字体设置集。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 定义一组从左到右文本的字体设置。
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// 为从右到左的文本定义另一组字体设置。
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// 我们可以使用 Bidi 标志来指示我们是否要添加文本
// 文档生成器是从右到左。当我们添加文本并将此标志设置为 true 时，
// 它将使用从右到左的字体设置集进行格式化。
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// 将标志设置为 false，然后添加从左到右的文本。
// 文档生成器将使用从左到右的字体设置集来格式化它们。
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
