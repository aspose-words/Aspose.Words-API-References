---
title: Font.NameBi
linktitle: NameBi
articleTitle: NameBi
second_title: Aspose.Words for .NET
description: 了解如何轻松设置和自定义从右到左语言文档的字体名称，从而提升可读性和设计感。立即优化您的文本！
type: docs
weight: 250
url: /zh/net/aspose.words/font/namebi/
---
## Font.NameBi property

返回或设置从右到左语言文档中的字体名称。

```csharp
public string NameBi { get; set; }
```

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

* property [Name](../name/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
