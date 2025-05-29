---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words for .NET
description: 探索字体填充属性，通过可自定义的填充格式增强文本的外观，获得精致、专业的外观。
type: docs
weight: 130
url: /zh/net/aspose.words/font/fill/
---
## Font.Fill property

获取填充格式[`Font`](../).

```csharp
public Fill Fill { get; }
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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
