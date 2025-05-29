---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.FillType 枚举，使用多种填充类型增强可填充对象，从而改进文档设计。
type: docs
weight: 1280
url: /zh/net/aspose.words.drawing/filltype/
---
## FillType enumeration

指定可填充对象的填充类型。

```csharp
public enum FillType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Solid | `1` | 实心填充。 |
| Patterned | `2` | 图案填充。 |
| Gradient | `3` | 渐变填充。 |
| Textured | `4` | 纹理填充。 |
| Background | `5` | 填充与背景相同。 |
| Picture | `6` | 图片填充。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
