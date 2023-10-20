---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: 用于 .NET 的 Aspose.Words
description: TextBox TextBoxWrapMode 财产. 确定文本如何在形状内换行 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

确定文本如何在形状内换行。

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## 评论

默认值为Square。

## 例子

演示如何设置文本框内容的换行模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// 将“TextBoxWrapMode”属性设置为“TextBoxWrapMode.None”以增加文本框的宽度
// 为了容纳文本，它是否足够大。
// 将“TextBoxWrapMode”属性设置为“TextBoxWrapMode.Square”即可
// 将所有文本包裹在文本框中，保留其尺寸。
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### 也可以看看

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
