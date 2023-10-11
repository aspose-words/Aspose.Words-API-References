---
title: Fill.Color
second_title: Aspose.Words for .NET API 参考
description: Fill 财产. 获取或设置一个 Color 对象该对象表示填充的前景色
type: docs
weight: 50
url: /zh/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

获取或设置一个 Color 对象，该对象表示填充的前景色。

```csharp
public Color Color { get; set; }
```

### 评论

该属性保留了 alpha 分量Color, 与[`ForeColor`](../forecolor/)属性，将其重置为完全不透明的颜色。

### 例子

演示如何将任何填充转换回实体填充。

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// 获取第一次运行的字体的填充对象。
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
* 命名空间 [Aspose.Words.Drawing](../../fill/)
* 部件 [Aspose.Words](../../../)


