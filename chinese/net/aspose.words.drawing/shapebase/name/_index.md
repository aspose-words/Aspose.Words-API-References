---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase Name 财产. 获取或设置可选的形状名称 在 C#.
type: docs
weight: 400
url: /zh/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

获取或设置可选的形状名称。

```csharp
public string Name { get; set; }
```

## 评论

默认为空字符串。

不能为空，但可以是空字符串。

## 例子

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
