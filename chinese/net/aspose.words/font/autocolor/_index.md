---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: 用于 .NET 的 Aspose.Words
description: Font AutoColor 财产. 返回用于自动颜色的文本的当前计算颜色黑色或白色 如果颜色不是自动则返回Color 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

返回用于“自动颜色”的文本的当前计算颜色（黑色或白色）。 如果颜色不是“自动”，则返回[`Color`](../color/).

```csharp
public Color AutoColor { get; }
```

## 评论

当文本具有“自动颜色”时，会自动计算文本的实际颜色 以便在背景颜色下可读。当您更改背景颜色时， 文本颜色将在 MS Word 中自动切换为黑色或白色，以最大限度地提高可读性。

## 例子

展示如何通过根据背景亮度自动选择文本颜色来提高可读性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果一个run的Font对象没有指定文字颜色，它会自动
// 根据背景颜色选择黑色或白色。
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// 文本的默认颜色是黑色。如果背景颜色较深，黑色文本将难以看清。
// 为了解决这个问题，AutoColor 属性将这个文本显示为白色。
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// 如果我们把背景改成浅色，黑色会更
// 适合文本颜色而不是白色，以便自动颜色将其显示为黑色。
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
