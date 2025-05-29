---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: 发现字体名称属性，轻松自定义和设置字体样式，增强设计的吸引力和可读性。
type: docs
weight: 230
url: /zh/net/aspose.words/font/name/
---
## Font.Name property

获取或设置字体的名称。

```csharp
public string Name { get; set; }
```

## 评论

获取时返回[`NameAscii`](../nameascii/)。

设置时，设置[`NameAscii`](../nameascii/)，[`NameBi`](../namebi/)，[`NameFarEast`](../namefareast/) 和[`NameOther`](../nameother/)到指定值。

## 例子

展示如何使用字体属性来格式化文本。

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

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
