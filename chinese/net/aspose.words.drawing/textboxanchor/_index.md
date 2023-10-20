---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.TextBoxAnchor 枚举. 指定用于形状文本垂直对齐的值 在 C#.
type: docs
weight: 1330
url: /zh/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

指定用于形状文本垂直对齐的值。

```csharp
public enum TextBoxAnchor
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Top | `0` | 文本与文本框顶部对齐。 |
| Middle | `1` | 文本与文本框的中间对齐。 |
| Bottom | `2` | 文本与文本框底部对齐。 |
| TopCentered | `3` | 文本与文本框的顶部中心对齐。 |
| MiddleCentered | `4` | 文本与文本框的中间居中对齐。 |
| BottomCentered | `5` | 文本与文本框底部居中对齐。 |
| TopBaseline | `6` | 文本与文本框的顶部基线对齐。 |
| BottomBaseline | `7` | 文本与文本框的底部基线对齐。 |
| TopCenteredBaseline | `8` | 文本与文本框顶部居中的基线对齐。 |
| BottomCenteredBaseline | `9` | 文本与文本框底部居中的基线对齐。 |

## 例子

演示如何垂直对齐文本框的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Top”
// 将此文本框中的文本与形状的顶部对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Middle”
// 将此文本框中的文本与形状的中心对齐。
// 将“VerticalAnchor”属性设置为“TextBoxAnchor.Bottom”
// 将此文本框中的文本与形状的底部对齐。
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// 从 Microsoft Word 2007 开始，文本框中文本的垂直对齐功能可用。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
