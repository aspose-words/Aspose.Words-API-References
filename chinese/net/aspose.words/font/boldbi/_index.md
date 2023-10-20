---
title: Font.BoldBi
linktitle: BoldBi
articleTitle: BoldBi
second_title: 用于 .NET 的 Aspose.Words
description: Font BoldBi 财产. 如果从右到左的文本格式为粗体则为 True 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/font/boldbi/
---
## Font.BoldBi property

如果从右到左的文本格式为粗体，则为 True。

```csharp
public bool BoldBi { get; set; }
```

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
