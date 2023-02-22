---
title: Font.ItalicBi
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 如果从右到左的文本格式为斜体则为真
type: docs
weight: 170
url: /zh/net/aspose.words/font/italicbi/
---
## Font.ItalicBi property

如果从右到左的文本格式为斜体，则为真。

```csharp
public bool ItalicBi { get; set; }
```

### 例子

演示如何为从右到左和从右到左的文本定义单独的字体设置集。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为从左到右的文本定义一组字体设置。
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

// 我们可以使用 Bidi 标志来指示我们是否要添加的文本
// 文档构建器是从右到左的。当我们将此标志设置为 true 添加文本时，
// 它将使用从右到左的字体设置集进行格式化。
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// 将标志设置为 false，然后添加从左到右的文本。
// 文档生成器将使用从左到右的字体设置设置这些格式。
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


