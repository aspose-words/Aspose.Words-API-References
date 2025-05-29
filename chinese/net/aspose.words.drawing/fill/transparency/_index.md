---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words for .NET
description: 将填充透明度从 0.0（不透明）调整到 1.0（透明），以便在设计中自定义视觉效果。立即提升项目的美感！
type: docs
weight: 200
url: /zh/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

获取或设置指定填充的透明度，值为 0.0（不透明）和 1.0（透明）之间的值。

```csharp
public double Transparency { get; set; }
```

## 评论

此属性与属性相反[`Opacity`](../opacity/)。

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
