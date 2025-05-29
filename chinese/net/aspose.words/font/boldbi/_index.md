---
title: Font.BoldBi
linktitle: BoldBi
articleTitle: BoldBi
second_title: Aspose.Words for .NET
description: 发现 BoldBi 属性，确保从右到左的文本以粗体显示，增强不同语言的可读性和用户体验。
type: docs
weight: 50
url: /zh/net/aspose.words/font/boldbi/
---
## Font.BoldBi property

如果从右到左的文本被格式化为粗体，则为真。

```csharp
public bool BoldBi { get; set; }
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

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
