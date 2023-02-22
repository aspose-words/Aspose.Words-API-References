---
title: DocumentBase.PageColor
second_title: Aspose.Words for .NET API 参考
description: DocumentBase 财产. 获取或设置文档的页面颜色这个属性是一个更简单的版本BackgroundShape.
type: docs
weight: 60
url: /zh/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

获取或设置文档的页面颜色。这个属性是一个更简单的版本[`BackgroundShape`](../backgroundshape/).

```csharp
public Color PageColor { get; set; }
```

### 评论

此属性提供了一种为文档指定纯色页面颜色的简单方法。 设置此属性会创建并设置适当的[`BackgroundShape`](../backgroundshape/).

如果没有设置页面颜色（例如文档中没有背景形状）返回 Empty.

### 例子

显示如何为文档的所有页面设置背景颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### 也可以看看

* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)


