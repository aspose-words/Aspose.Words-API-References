---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words for .NET
description: 探索 ShapeBase AlternativeText 属性，它通过为图形提供描述性文本来增强可访问性，从而改善用户体验和 SEO。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

定义要显示的替代图形的文本。

```csharp
public string AlternativeText { get; set; }
```

## 评论

默认值为空字符串。

## 例子

展示如何使用形状的替代文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// 我们可以通过右键单击形状，然后通过“设置自选图形格式”->“替代文本”来访问形状的替代文本。
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// 将文档保存为 HTML，然后删除属于我们形状的链接图像。
// 读取我们的 HTML 的浏览器将显示替代文本来代替缺失的图像。
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
