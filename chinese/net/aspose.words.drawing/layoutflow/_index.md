---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words for .NET
description: 发现 Aspose.Words.Drawing.LayoutFlow 枚举来控制文本框中的文本布局，轻松增强文档设计和可读性。
type: docs
weight: 1430
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

演示如何向文本框添加文本并更改其方向

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

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
