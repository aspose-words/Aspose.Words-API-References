---
title: ShapeBase.AlternativeText
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 定义要显示的替代文本而不是图形
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

定义要显示的替代文本而不是图形。

```csharp
public string AlternativeText { get; set; }
```

### 评论

默认值为空字符串。

### 例子

显示如何使用形状的替代文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// 我们可以通过右键单击形状访问替代文本，然后通过“设置自选图形格式”-> “替代文字”。
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// 将文档保存为 HTML，然后删除属于我们形状的链接图像。
// 正在读取我们的 HTML 的浏览器将显示替代文本以代替丢失的图像。
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


