---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: 发现 Font Bidi 属性，控制从右到左的文本特性，以增强网页设计的可读性和用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words/font/bidi/
---
## Font.Bidi property

指定此运行的内容是否应具有从右到左的特性。

```csharp
public bool Bidi { get; set; }
```

## 评论

此属性启用时，不得与强从左到右的文本一起使用。此条件下的任何行为均未指定。 此属性禁用时，不得与强从右到左的文本一起使用。此条件下的任何行为均未指定。

当显示此运行的内容时，所有字符都应被视为复杂脚本字符，以用于 formatting 目的。这意味着[`BoldBi`](../boldbi/)，[`ItalicBi`](../italicbi/)，[`SizeBi`](../sizebi/)并且在渲染此运行时将使用相应的字体名称 。

此外，当显示此运行的内容时，此属性充当从右到左覆盖的 characters ，这些 characters 被归类为“弱类型”和“中性类型”。

## 例子

展示如何为从右到左和从右到左的文本定义单独的字体设置集。

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

// 我们可以使用 Bidi 标志来指示我们即将添加的文本
// 使用文档构建器时，文本的显示顺序是从右到左。当我们添加文本时，如果此标志设置为 true，
// 它将使用从右到左的字体设置进行格式化。
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// 将标志设置为 false，然后添加从左到右的文本。
// 文档构建器将使用从左到右的字体设置来格式化这些内容。
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
