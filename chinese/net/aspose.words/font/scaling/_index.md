---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words for .NET
description: 发现字体缩放属性以百分比调整字符宽度，增强文本的可读性和项目的设计灵活性。
type: docs
weight: 320
url: /zh/net/aspose.words/font/scaling/
---
## Font.Scaling property

获取或设置字符宽度缩放百分比。

```csharp
public int Scaling { get; set; }
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
