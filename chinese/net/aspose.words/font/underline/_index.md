---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: 探索“字体下划线”属性，自定义文本样式。轻松设置和修改下划线类型，提升设计中的排版效果。
type: docs
weight: 540
url: /zh/net/aspose.words/font/underline/
---
## Font.Underline property

获取或设置应用于字体的下划线类型。

```csharp
public Underline Underline { get; set; }
```

## 例子

展示如何配置文本下划线的样式和颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

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

* enum [Underline](../../underline/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
