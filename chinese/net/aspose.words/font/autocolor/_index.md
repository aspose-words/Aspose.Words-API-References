---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: 用于 .NET 的 Aspose.Words
description: Font AutoColor 财产. 返回当前计算的用于自动颜色的文本颜色黑色或白色 如果颜色不是自动则返回Color 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

返回当前计算的用于“自动颜色”的文本颜色（黑色或白色）。 如果颜色不是“自动”则返回[`Color`](../color/).

```csharp
public Color AutoColor { get; }
```

## 评论

当文本具有“自动颜色”时，会自动计算文本的实际颜色 ，以便在背景颜色的衬托下可读。当您更改背景颜色时， MS Word 中的文本颜色将自动切换为黑色或白色，以最大限度地提高可读性。

## 例子

演示如何通过根据背景亮度自动选择文本颜色来提高可读性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果运行的 Font 对象没有指定文本颜色，它将自动
// 根据背景颜色选择黑色或白色。
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// 文本的默认颜色是黑色。如果背景颜色较深，黑色文本将很难看清。
// 为了解决这个问题，AutoColor 属性将以白色显示该文本。
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// 如果我们将背景改为浅色，黑色会更显眼
// 比白色更合适的文本颜色，以便自动颜色将其显示为黑色。
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
