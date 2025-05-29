---
title: Fill.FillType
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words for .NET
description: 了解如何有效地设置 FillType 属性并使用可自定义的填充选项增强您的设计以获得更好的视觉效果。
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/fill/filltype/
---
## Fill.FillType property

获取填充类型。

```csharp
public FillType FillType { get; }
```

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

* enum [FillType](../../filltype/)
* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
