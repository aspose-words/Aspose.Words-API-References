---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: 用于 .NET 的 Aspose.Words
description: TextBox NoTextRotation 财产. 获取或设置一个布尔值指示旋转形状时 TextBox 的文本不应旋转 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

获取或设置一个布尔值，指示旋转形状时 TextBox 的文本不应旋转。

```csharp
public bool NoTextRotation { get; set; }
```

## 评论

默认值为`错误的`

## 例子

显示如何在形状旋转时禁用文本旋转。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### 也可以看看

* class [TextBox](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
