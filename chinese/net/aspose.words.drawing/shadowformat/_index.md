---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ShadowFormat，增强对象阴影效果。使用可自定义的阴影格式选项，提升您的文档设计水平。
type: docs
weight: 1620
url: /zh/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

表示对象的阴影格式。

要了解更多信息，请访问[使用图形元素](https://docs.aspose.com/words/net/working-with-graphic-elements/)文档文章。

```csharp
public class ShadowFormat
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | 获得Color表示阴影颜色的对象。 默认值为Black. |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | 获取或设置指定的[`ShadowType`](../shadowtype/)对于 ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | 返回`真的`如果应用于此实例的格式可见。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | 清除阴影格式。 |

## 例子

展示如何获取阴影颜色。

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
