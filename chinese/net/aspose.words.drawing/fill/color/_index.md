---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 探索填充颜色属性，使用颜色对象轻松自定义设计的前景色，增强项目的视觉吸引力。
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

获取或设置代表填充前景色的 Color 对象。

```csharp
public Color Color { get; set; }
```

## 评论

此属性保留Color, 与[`ForeColor`](../forecolor/)属性，将其重置为完全不透明的颜色。

## 例子

展示如何将任何填充转换回实心填充。

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// 获取第一个 Run 的 Font 的 Fill 对象。
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// 检查字体的填充属性。
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// 将填充类型更改为均匀的绿色实心。
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
