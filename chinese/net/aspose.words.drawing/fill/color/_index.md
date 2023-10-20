---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: 用于 .NET 的 Aspose.Words
description: Fill Color 财产. 获取或设置表示填充前景色的 Color 对象 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

获取或设置表示填充前景色的 Color 对象。

```csharp
public Color Color { get; set; }
```

## 例子

显示如何将任何填充转换回实体填充。

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// 获取第一个 Run 的 Font 的 Fill 对象。
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// 检查字体的填充属性。
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// 将填充类型更改为具有统一绿色的实心。
fill.Solid(Color.Green);
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
