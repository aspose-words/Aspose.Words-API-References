---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words for .NET
description: 使用 NoTextRotation 属性控制文本框中的文本旋转。即使形状旋转，也能确保文本清晰易读。提升您的设计！
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

获取或设置一个布尔值，指示当形状旋转时，TextBox 的文本不应旋转。

```csharp
public bool NoTextRotation { get; set; }
```

## 评论

默认值为`错误的`

## 例子

展示如何在形状旋转时禁用文本旋转。

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
