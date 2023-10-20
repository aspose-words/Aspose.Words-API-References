---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.LayoutFlow 枚举. 确定文本框中文本布局的流程 在 C#.
type: docs
weight: 1100
url: /zh/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

确定文本框中文本布局的流程。

```csharp
public enum LayoutFlow
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Horizontal | `0` | 文本水平显示。 |
| TopToBottomIdeographic | `1` | 表意文字垂直显示。 |
| BottomToTop | `2` | 文本垂直显示。 |
| TopToBottom | `3` | 文本垂直显示。 |
| HorizontalIdeographic | `4` | 表意文字水平显示。 |
| Vertical | `5` | 文本垂直显示。 |

## 例子

演示如何将文本添加到文本框并更改其方向

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100, 
    Height = 100,
    TextBox = { LayoutFlow = LayoutFlow.BottomToTop }
};

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### 也可以看看

* property [LayoutFlow](../textbox/layoutflow/)
* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
