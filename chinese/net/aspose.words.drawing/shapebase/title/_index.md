---
title: ShapeBase.Title
linktitle: Title
articleTitle: Title
second_title: 用于 .NET 的 Aspose.Words
description: ShapeBase Title 财产. 获取或设置当前形状对象的标题标题 在 C#.
type: docs
weight: 530
url: /zh/net/aspose.words.drawing/shapebase/title/
---
## ShapeBase.Title property

获取或设置当前形状对象的标题（标题）。

```csharp
public string Title { get; set; }
```

## 评论

默认为空字符串。

不能为空，但可以是空字符串。

## 例子

显示如何设置形状的标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个形状，给它一个标题，然后将它添加到文档中。
Shape shape = new Shape(doc, ShapeType.Cube);
shape.Width = 200;
shape.Height = 200;
shape.Title = "My cube";

builder.InsertNode(shape);

// 当我们保存一个带有标题的形状的文档时，
// Aspose.Words 会将该标题存储在形状的替代文本中。
doc.Save(ArtifactsDir + "Shape.Title.docx");

doc = new Document(ArtifactsDir + "Shape.Title.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(string.Empty, shape.Title);
Assert.AreEqual("Title: My cube", shape.AlternativeText);
```

### 也可以看看

* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
