---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: 用于 .NET 的 Aspose.Words
description: Fill Solid 方法. 将填充设置为统一颜色 在 C#.
type: docs
weight: 250
url: /zh/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

将填充设置为统一颜色。

```csharp
public void Solid()
```

## 评论

使用此方法将任何填充转换回实心填充。

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

将填充设置为指定的统一颜色。

```csharp
public void Solid(Color color)
```

## 评论

使用此方法将任何填充转换回实心填充。

## 例子

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
