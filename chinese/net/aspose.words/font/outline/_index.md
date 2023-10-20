---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: 用于 .NET 的 Aspose.Words
description: Font Outline 财产. 如果字体格式为轮廓则为 True 在 C#.
type: docs
weight: 290
url: /zh/net/aspose.words/font/outline/
---
## Font.Outline property

如果字体格式为轮廓，则为 True。

```csharp
public bool Outline { get; set; }
```

## 例子

演示如何创建一系列格式化为轮廓的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置轮廓标志以将文本的填充颜色更改为白色
// 以文本的原始颜色在每个字符周围留下细轮廓。
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
