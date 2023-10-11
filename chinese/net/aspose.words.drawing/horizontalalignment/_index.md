---
title: Enum HorizontalAlignment
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.HorizontalAlignment 枚举. 指定浮动形状文本框架或浮动表格的水平对齐方式
type: docs
weight: 1030
url: /zh/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

指定浮动形状、文本框架或浮动表格的水平对齐方式。

```csharp
public enum HorizontalAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 对象被显式定位，通常使用其 **左边**属性. |
| Default | `0` | 与相同None. |
| Left | `1` | 指定对象应与水平对齐基准左对齐。 |
| Center | `2` | 指定对象应相对于水平对齐基准居中。 |
| Right | `3` | 指定对象应与水平对齐基准右对齐。 |
| Inside | `4` | 指定对象应位于水平对齐基准的内部。 |
| Outside | `5` | 指定对象应位于水平对齐基础之外。 |

### 例子

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

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)


