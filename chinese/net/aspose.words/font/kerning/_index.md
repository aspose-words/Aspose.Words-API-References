---
title: Font.Kerning
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置字距调整开始时的字体大小
type: docs
weight: 180
url: /zh/net/aspose.words/font/kerning/
---
## Font.Kerning property

获取或设置字距调整开始时的字体大小。

```csharp
public double Kerning { get; set; }
```

### 例子

演示如何指定字距调整开始生效的字体大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// 设置构建器的字体大小以及字距调整生效的最小大小。
// 字体大小低于字距调整阈值，因此下面的运行将不会进行字距调整。
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// 设置字距调整阈值，使构建器的当前字体大小位于其之上。
// 我们从此时添加的任何文本都将应用字距调整。字符之间的空格
// 将进行调整，通常会产生稍微更美观的文本运行。
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


