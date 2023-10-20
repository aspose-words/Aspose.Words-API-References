---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: 用于 .NET 的 Aspose.Words
description: Font Size 财产. 获取或设置字体大小以磅为单位 在 C#.
type: docs
weight: 340
url: /zh/net/aspose.words/font/size/
---
## Font.Size property

获取或设置字体大小（以磅为单位）。

```csharp
public double Size { get; set; }
```

## 例子

演示如何使用其字体属性设置文本串的格式。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

演示如何使用 DocumentBuilder 插入格式化文本。

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

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
