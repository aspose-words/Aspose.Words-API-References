---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 探索“字体颜色”属性，轻松自定义设计中的文本颜色。使用鲜艳夺目的色调，提升可读性和美观度！
type: docs
weight: 70
url: /zh/net/aspose.words/font/color/
---
## Font.Color property

获取或设置字体的颜色。

```csharp
public Color Color { get; set; }
```

## 例子

展示如何使用 DocumentBuilder 插入格式化文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定字体格式，然后添加文本。
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

显示如何插入超链接字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// 插入超链接并使用自定义格式强调它。
// 超链接将是一段可点击的文本，它将带我们到 URL 中指定的位置。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// 按住 Ctrl 键并左键单击 Microsoft Word 中文本中的链接将通过新的 Web 浏览器窗口带我们进入 URL。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
