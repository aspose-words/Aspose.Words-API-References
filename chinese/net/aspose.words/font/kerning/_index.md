---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: 用于 .NET 的 Aspose.Words
description: Font Kerning 财产. 获取或设置字距调整开始时的字体大小 在 C#.
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

显示如何指定字距调整开始生效的字体大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// 设置构建器的字体大小，以及字距调整生效的最小大小。
// 字体大小低于字距调整阈值，因此运行波纹管将没有字距调整。
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// 设置字距调整阈值，使构建器的当前字体大小高于它。
// 我们从这一点添加的任何文本都将应用字距调整。字符之间的空格
// 将被调整，通常会产生更美观的文本运行。
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
