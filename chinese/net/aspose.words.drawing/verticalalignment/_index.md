---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.VerticalAlignment 枚举. 指定浮动形状文本框架或浮动表格的垂直对齐方式 在 C#.
type: docs
weight: 1380
url: /zh/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

指定浮动形状、文本框架或浮动表格的垂直对齐方式。

```csharp
public enum VerticalAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 对象被显式定位，通常使用其**顶部**属性. |
| Top | `1` | 指定对象应位于垂直对齐底座的顶部。 |
| Center | `2` | 指定对象应相对于垂直对齐基准居中。 |
| Bottom | `3` | 指定对象应位于垂直对齐底座的底部。 |
| Inside | `4` | 指定对象应位于水平对齐基准的内部。 |
| Outside | `5` | 指定对象应位于垂直对齐基准之外。 |
| Inline | `-1` | 未记录。似乎是浮动段落和表格的可能值。 |
| Default | `0` | 与相同None. |

## 例子

演示如何将浮动图像插入到页面中央。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个浮动图像，该图像将出现在重叠文本后面并将其与页面中心对齐。
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### 也可以看看

* property [VerticalAlignment](../shapebase/verticalalignment/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
