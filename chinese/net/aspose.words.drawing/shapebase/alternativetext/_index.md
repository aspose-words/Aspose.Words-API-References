---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase AlternativeText 财产. 定义要显示的替代文本而不是图形 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

定义要显示的替代文本，而不是图形。

```csharp
public string AlternativeText { get; set; }
```

## 评论

默认值为空字符串。

## 例子

演示如何使用形状的替代文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// 我们可以通过右键单击形状来访问形状的替代文本，然后通过“设置自选图形格式”-> “替代文本”。
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// 将文档保存为 HTML，然后删除属于我们形状的链接图像。
// 正在读取 HTML 的浏览器将显示替代文本来代替丢失的图像。
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
