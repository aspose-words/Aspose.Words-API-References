---
title: Font.LocaleIdBi
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置格式化的从右到左字符的区域设置标识符语言
type: docs
weight: 210
url: /zh/net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

获取或设置格式化的从右到左字符的区域设置标识符（语言）。

```csharp
public int LocaleIdBi { get; set; }
```

### 评论

有关区域设置标识符的列表，请参阅 https://msdn.microsoft.com/en-us/library/cc233965.aspx

### 例子

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
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


