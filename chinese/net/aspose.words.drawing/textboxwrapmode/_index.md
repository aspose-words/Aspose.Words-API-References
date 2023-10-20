---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.TextBoxWrapMode 枚举. 指定文本在形状内的换行方式 在 C#.
type: docs
weight: 1340
url: /zh/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

指定文本在形状内的换行方式。

```csharp
public enum TextBoxWrapMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Square | `0` | 文本环绕在形状内。 |
| None | `2` | 文本未包裹在形状内。 |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
