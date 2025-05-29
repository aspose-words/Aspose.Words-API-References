---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words for .NET
description: 探索字体字距调整属性，控制字距调整的开始时间，以获得最佳的文本清晰度和设计感。精准提升您的排版效果！
type: docs
weight: 180
url: /zh/net/aspose.words/font/kerning/
---
## Font.Kerning property

获取或设置字距调整开始时的字体大小。

```csharp
public double Kerning { get; set; }
```

## 例子

展示如何指定字距调整开始生效的字体大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// 设置构建器的字体大小，以及字距调整生效的最小尺寸。
// 字体大小低于字距调整阈值，因此下面的运行将不会进行字距调整。
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// 设置字距调整阈值，以便构建器的当前字体大小高于该阈值。
// 从此处添加的任何文本都将应用字距调整。字符之间的空格
// 将会进行调整，通常会导致文本运行更加美观。
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
