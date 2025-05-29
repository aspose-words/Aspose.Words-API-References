---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words for .NET
description: 探索字体间距属性，轻松调整字符间距（以点为单位）。通过精确的排版控制，提升可读性和设计感。
type: docs
weight: 390
url: /zh/net/aspose.words/font/spacing/
---
## Font.Spacing property

返回或设置字符之间的间距（以点为单位）。

```csharp
public double Spacing { get; set; }
```

## 例子

展示如何设置字符的水平缩放和间距。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加文本并将字符宽度增加到 150%。
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// 添加文本运行并在每个字符之间添加 1pt 的额外水平间距。
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// 添加文本并将字符间距缩小 1pt。
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
